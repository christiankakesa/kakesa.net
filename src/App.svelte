<script>
	import {
		Avatar,
		Badge,
		Divider,
		Button,
		Icon,
		MaterialApp,
		Ripple,
	} from "svelte-materialify";
	import {
		mdiHome,
		mdiGithub,
		mdiTwitter,
		mdiLinkedin,
		mdiStackOverflow,
		mdiAccountBox,
	} from "@mdi/js";
	import md5 from "md5";

	let gravatarHash = md5("christian.kakesa@gmail.com");
	let gravatarLink = "https://www.gravatar.com/avatar/" + gravatarHash;
</script>

<MaterialApp>
	<div class="elevation-24 rounded pa-3">
		<h1 class="d-flex justify-center">
			Christian Kakesa
			<Divider vertical inset class="ml-4 mr-4" />
			<Badge class="success-color" dot bottom offsetX={10} offsetY={10}>
				<Avatar><img src={gravatarLink} alt="profile" /></Avatar>
			</Badge>
		</h1>

		<div class="d-flex flex-column">
			<a
				href="https://www.linkedin.com/in/christiankakesa/"
				target="_blank"
				title="LinkedIn"
			>
				<Button block size="x-large">
					<Icon path={mdiLinkedin} /> @christiankakesa
				</Button>
			</a>
		</div>

		<div class="d-flex flex-column">
			<a
				href="https://github.com/christiankakesa"
				target="_blank"
				title="Github"
			>
				<Button block size="x-large">
					<Icon path={mdiGithub} /> @christiankakesa
				</Button>
			</a>
		</div>

		<div class="d-flex flex-column">
			<a
				href="https://twitter.com/christiankakesa"
				target="_blank"
				title="Twitter"
			>
				<Button block size="x-large">
					<Icon path={mdiTwitter} /> @christiankakesa
				</Button>
			</a>
		</div>

		<div class="d-flex flex-column">
			<a
				href="https://blog.kakesa.net"
				target="_blank"
				title="Blog, Website"
			>
				<Button block size="x-large">
					<Icon path={mdiHome} class="mr-3" /> blog.kakesa.net
				</Button>
			</a>
		</div>

		<div class="d-flex flex-column">
			<a
				href="https://stackoverflow.com/users/592319/christian-kakesa"
				target="_blank"
				title="stackoverflow"
			>
				<Button block size="x-large">
					<Icon path={mdiStackOverflow} /> christian-kakesa
				</Button>
			</a>
		</div>
		<div
			class="text-center pt-8 pb-8 text-h4 elevation-2"
			use:Ripple={{ centered: true }}
		>
			Blockchain and Crypto Projects
		</div>
		<div class="d-flex flex-column">
			<a
				href="https://twitter.com/theminercrabs"
				target="_blank"
				title="A DAO for Crabada PlayToEarn GameFi"
			>
				<Button block size="x-large"
					>TheMinerCrabs DAO : Crabada (🦀,🦀)🔺</Button
				>
			</a>
			<a
				href="https://github.com/Axentro/minaxnt"
				target="_blank"
				title="MinAXNT for the Axentro blockchain"
			>
				<Button block size="x-large"
					>MinAXNT, CPU only mining for Axentro</Button
				>
			</a>
		</div>
		<div
			class="text-center pt-8 pb-8 text-h4 elevation-2"
			use:Ripple={{ centered: true }}
		>
			Projects
		</div>
		<div class="d-flex flex-column">
			<a
				href="https://congopro.com"
				target="_blank"
				title="Congopro, Annuaire des entreprises et professionnels"
			>
				<Button block size="x-large">Congopro</Button>
			</a>
		</div>
	</div>
</MaterialApp>

<style>
	h1 {
		color: #000;
	}
	a:link,
	a:hover,
	a:visited,
	a:active {
		text-decoration: none;
	}
</style>
