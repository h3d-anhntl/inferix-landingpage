<script lang="ts">
	import WhyInferix from '$images/icons/WhyInferix.svg';
	import Performance from '$images/png/Performance.png';
	import Scalability from '$images/png/Scalability.png';
	import Utilization from '$images/png/Utilization.png';
	import Intergration from '$images/png/Intergration.png';
	const reasons = [
		{
			icon: Performance,
			title: 'High - Performance Rendering',
			des: 'Inferix harnesses the combined power of decentralized GPUs to deliver high - performance rendering, allowing for faster and more efficient processing of complex visual content'
		},
		{
			icon: Scalability,
			title: 'Seamless Scalability',
			des: 'Scale your rendering tasks effortlessly by tapping into a distributed network of GPUs. Inferix ensures that as your project grows. You’ll have the computational resources you need'
		},
		{
			icon: Utilization,
			title: 'Cost - Efficient Resource Utilization',
			des: 'Inferix’s decentralized approach optimizes usage, allowing you to use available GPUs without investing in costly hardware upgrades.'
		},
		{
			icon: Intergration,
			title: 'Secure Blockchain Integration',
			des: 'Built on blockchain technology, Inferix ensures secure and transparent usage of GPU resources, providing a reliable and trusted environment.'
		}
	];
</script>

<div
	id="network"
	class="md:pt-[142px] pt-[50px] pb-[185px] whyInferixContainer md:px-0 px-5 box-border"
>
	<div class="container mx-auto">
		<img src={WhyInferix} alt="why inferix" class="mx-auto" />
		<div
			class="mt-[60px] grid lg:grid-cols-4 lg:grid-rows-1 md:grid-cols-2 md:grid-rows-2 grid-cols-1 grid-rows-4 gap-4 reasonContainer w-full"
		>
			{#each reasons as reason}
				<div class="">
					<div
						class="font-pre inset-0 flex flex-col items-center box-border text-center w-full h-full rounded-[28px] z-10"
					>
						<img src={reason.icon} alt="performance icon" />
						<p class="text-white text-[2rem] font-extrabold tilte">{reason.title}</p>
						<p class="text-normalGrey font-normal text-lg mt-4">
							{reason.des}
						</p>
					</div>
				</div>
			{/each}
		</div>
	</div>
</div>

<style lang="postcss">
	.whyInferixContainer {
		background: linear-gradient(180deg, #000 0%, #101010 100%);
	}
	.reasonContainer > div:nth-child(1) > div {
		padding: 25px 32px 44px 33px;
	}
	.reasonContainer > div:nth-child(1) > .title {
		margin-top: 5px;
	}
	.reasonContainer > div:nth-child(2) > div {
		padding: 38px 33px 63px 34px;
	}
	.reasonContainer > div:nth-child(2) > .title {
		margin-top: 28px;
	}
	.reasonContainer > div:nth-child(3) > div {
		padding: 38px 35px 62px 32px;
	}
	.reasonContainer > div:nth-child(3) > .title {
		margin-top: 18px;
	}
	.reasonContainer > div:nth-child(4) > div {
		padding: 32px 45px 39px 46px;
	}
	.reasonContainer > div:nth-child(4) > .title {
		margin-top: 6px;
	}

	.reasonContainer > div {
		position: relative;
		border-radius: 28px;
	}

	.reasonContainer > div::before {
		content: '';
		position: absolute;
		inset: 0;
		width: 100%;
		border-radius: 28px;
		padding: 1.5px;
		-webkit-mask: linear-gradient(#fff 0 0) content-box, /* [1] */ linear-gradient(#fff 0 0); /* [2] */
		-webkit-mask-composite: xor;
		mask-composite: exclude;
	}
	.reasonContainer > div:nth-child(1)::before {
		background: linear-gradient(120deg, rgba(95, 206, 93, 1) 0%, rgba(255, 255, 255, 0.16) 100%);
	}
	.reasonContainer > div:nth-child(n + 2)::before {
		background: linear-gradient(120deg, rgba(95, 206, 93, 1) 0%, rgba(0, 0, 0, 0) 100%);
	}
	@media screen and (min-width: 1050px) and (max-width: 1280px) {
		.reasonContainer {
			display: flex;
		}
		.reasonContainer > div {
			width: 24%;
		}
	}
</style>
