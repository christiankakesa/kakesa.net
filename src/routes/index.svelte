<script>
	import {
		Avatar,
		Badge,
		Menu,
		NavigationDrawer,
		Divider,
		Button,
		Icon,
		MaterialApp,
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
	<h1 class="d-flex justify-center">
		Christian Kakesa
		<Divider vertical inset class="ml-4 mr-4" />
		<Badge class="success-color" dot bottom offsetX={10} offsetY={10}>
			<Avatar><img src={gravatarLink} alt="profile" /></Avatar>
		</Badge>
	</h1>
	<div>
		<div class="d-flex flex-column">
			<a
				href="https://blog.kakesa.net"
				target="_blank"
				title="Blog, Website"
			>
				<Button tile block>
					<Icon path={mdiHome} class="mr-3" /> blog.kakesa.net
				</Button>
			</a>
		</div>

		<div class="d-flex flex-column">
			<a href="https://github.com/fenicks" target="_blank" title="Github">
				<Button block>
					<Icon path={mdiGithub} /> @fenicks
				</Button>
			</a>
		</div>

		<div class="d-flex flex-column">
			<a
				href="https://twitter.com/christiankakesa"
				target="_blank"
				title="Twitter"
			>
				<Button block>
					<Icon path={mdiTwitter} /> @christiankakesa
				</Button>
			</a>
		</div>

		<div class="d-flex flex-column">
			<a
				href="https://www.linkedin.com/in/christiankakesa/"
				target="_blank"
				title="LinkedIn"
			>
				<Button block>
					<Icon path={mdiLinkedin} /> @christiankakesa
				</Button>
			</a>
		</div>

		<div class="d-flex flex-column">
			<a
				href="https://stackoverflow.com/users/592319/christian-kakesa"
				target="_blank"
				title="stackoverflow"
			>
				<Button block>
					<Icon path={mdiStackOverflow} /> christian-kakesa
				</Button>
			</a>
		</div>
		<Divider />
		<div class="d-flex flex-column">
			<Badge class="info-color" bordered offsetX={24} offsetY={24}>
				<Button class="info-color" block>Projects</Button>
				<span slot="badge">
					<Icon path={mdiAccountBox} />
				</span>
			</Badge>
		</div>
		<div class="d-flex flex-column">
			<a href="https://kioo.fi/" target="_blank">
				<Button block>$KIOO Reflect Token</Button>
			</a>
			<a href="/#" target="_blank">
				<Button block>(soon) KiooVerse</Button>
			</a>
			<a href="/#" target="_blank">
				<Button block>(soon) Kioo Airdrop</Button>
			</a>
			<a
				href="https://twitter.com/theminercrabs"
				target="_blank"
				title="A DAO for Crabada PlayToEarn GameFi"
			>
				<Button block>TheMinerCrabs DAO</Button>
			</a>
			<a
				href="https://congopro.com"
				target="_blank"
				title="Congopro, Annuaire des entreprises et professionnels"
			>
				<Button block>Congopro</Button>
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
