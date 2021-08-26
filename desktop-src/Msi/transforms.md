---
description: A propriedade transformações é uma lista das transformações que o instalador aplica ao instalar o pacote.
ms.assetid: da20f99e-3022-4382-97bb-8f1206072347
title: Propriedade transformações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f873e439ef9542efa618a8e86c9667a3c962939f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474312"
---
# <a name="transforms-property"></a>Propriedade transformações

A propriedade **TRANSformações** é uma lista das transformações que o instalador aplica ao instalar o pacote. O instalador aplica as transformações na mesma ordem em que estão listadas na propriedade. As transformações podem ser especificadas por seu nome de arquivo ou caminho completo. Para especificar várias transformações, separe cada nome de arquivo ou caminho completo com um ponto-e-vírgula (;). Por exemplo, para aplicar três transformações a um pacote, defina **TRANSformações** para uma lista de nomes de arquivo ou para uma lista de caminhos completos.

``` syntax
TRANSFORMS=transform1.mst;transform2.mst;transform3.mst
TRANSFORMS=\\server\share\path\transform1.mst;\\server2\share2\path2\transform2.mst;\\server3\share3\path3\transform3.mst
```

Você pode indicar que um arquivo de transformação é inserido em um armazenamento do arquivo de .msi, e não como um arquivo autônomo, prefixando o nome do arquivo com dois-pontos (:). Por exemplo, o exemplo a seguir indica que transform1. MST e transform2. MST são inseridos dentro do arquivo de .msi e que transform3. MST é um arquivo autônomo.

``` syntax
TRANSFORMS=:transform1.mst;:transform2.mst;transform3.mst
```

O instalador requer as transformações listadas em **TRANSformações** em cada instalação, anúncio, instalação sob demanda ou instalação de manutenção do pacote. A política de [política do TransformsSecure](transformssecure-policy.md) , a propriedade **transformações** e o primeiro caractere da cadeia de **transformações** informa ao instalador como lidar com a resiliência da origem dos arquivos de transformação autônomos. Windows O instalador trata da configuração da [política TransformsAtSource](transformsatsource-policy.md) ou [**TransformsAtSource**](transformsatsource.md) da mesma forma que a política TransformsSecure e [**TransformsSecure**](transformssecure.md). Observe que as transformações inseridas no arquivo de .msi não são armazenadas em cache e são sempre obtidas do pacote.




| Propriedade transformações | Transformações seguras | Caching e resiliência | 
|---------------------|-------------------|------------------------|
| @ [<em>lista de nomes de FileNames</em>] exemplo:<br /> @transform1.mst; transform2. MST; transform3. MST<br /> | Nenhum efeito. | <a href="secure-at-source-transforms.md">Transformações de origem segura</a>. A origem das transformações deve estar na raiz da origem do pacote. Quando o pacote é instalado ou anunciado, o instalador salva as transformações no computador do usuário em um cache em que o usuário não tem acesso de gravação. Se a cópia local da transformação ficar indisponível, o instalador procurará uma origem para restaurar o cache. O método é o mesmo que pesquisar a lista de origem de um arquivo de .msi. Consulte <a href="source-resiliency.md">resiliência da origem</a>. | 
| |[<em>lista de caminhos</em>] Exemplo<br /><pre class="syntax" data-space="preserve"><code>|\\server\share\path\transform1.MST; \\ server2\share2\path2\transform2.mst</code></pre> | Nenhum efeito. | <a href="secure-full-path-transforms.md">Alta segurança – transformações de caminho completo</a>. A origem de cada transformação deve estar no caminho completo passado para <strong>TRANSformações</strong>. A origem da transformação não precisa estar localizada na origem do pacote. Quando o pacote é instalado ou anunciado, o instalador salva as transformações no computador do usuário em um cache em que o usuário não tem acesso de gravação. Se a cópia local da transformação ficar indisponível, o instalador só poderá restaurar o cache da origem no caminho especificado. | 
| [<em>lista de nomes de FileName</em>] O primeiro caractere não é @ ou |.<br /> Exemplo:<br /> transform1. MST; deform2. MST; transform3. MST<br /> | <a href="transformssecure-policy.md">Política TransformsSecure</a> ou <a href="transformssecure.md"><strong>TransformsSecure</strong></a> definida como 1 ou<br /><a href="transformsatsource-policy.md">Política TransformsAtSource</a> ou <a href="transformsatsource.md"><strong>TransformsAtSource</strong></a> definida como 1.<br /> | Se <strong>TRANSformações</strong> for uma lista de nomes de File, o instalador os tratará como <a href="secure-at-source-transforms.md">transformações de origem segura</a>. Se <strong>TRANSformações</strong> for uma lista de caminhos completos, o instalador os tratará como <a href="secure-full-path-transforms.md">transformações de caminho completo seguro</a>.<br /> | 
| [<em>lista de nomes de FileName</em>] O primeiro caractere não é @ ou |.<br /> Exemplo:<br /> transform1. MST; deform2. MST; transform3. MST<br /> | A <a href="transformssecure-policy.md">política TransformsSecure</a> e <a href="transformssecure.md"><strong>TransformsSecure</strong></a> não estão definidas e<br />A <a href="transformsatsource-policy.md">política TransformsAtSource</a> e <a href="transformsatsource.md"><strong>TransformsAtSource</strong></a> não estão definidas.<br /> | <a href="unsecured-transforms.md">Transformações não seguras</a>. A origem das transformações deve estar na raiz da origem do pacote. Quando o pacote é instalado ou anunciado por usuário, o instalador salva as transformações no perfil do usuário. Isso permite que um usuário faça roaming entre computadores mantendo suas personalizações. Para uma instalação por computador, a transformação é salva na pasta%windir%\Installer. Se a cópia local da transformação ficar indisponível, o instalador procurará uma origem para restaurar o cache. O método é o mesmo que pesquisar a lista de origem de um arquivo de .msi. Consulte <a href="source-resiliency.md">resiliência da origem</a>. | 
| [<em>lista de caminhos</em>] O primeiro caractere não é @ ou |.<br /> Exemplo:<br /><pre class="syntax" data-space="preserve"><code>\\server\share\path\transform1.mst;\\server2\share2\path2\transform2.mst.</code></pre> | A <a href="transformsatsource-policy.md">política TransformsAtSource</a> e <a href="transformssecure.md"><strong>TRANSFORMSSECURE</strong></a> não estão definidas e<br />A <a href="transformsatsource-policy.md">política TransformsAtSource</a> e a <a href="transformssecure.md"><strong>TRANSFORMSSECURE</strong></a> não estão definidas..<br /> | <a href="unsecured-transforms.md">Transformações não seguras</a>. Quando o pacote é instalado ou anunciado por usuário, o instalador salva as transformações no perfil do usuário. Isso permite que um usuário faça roaming entre computadores mantendo suas personalizações. Para uma instalação por computador, a transformação é salva na pasta%windir%\Installer. Se a cópia local da transformação ficar indisponível, o instalador procurará uma origem para restaurar o cache. O método é o mesmo que pesquisar a lista de origem de um arquivo de .msi. Consulte <a href="source-resiliency.md">resiliência da origem</a>. | 




 

Você não pode usar nomes de filePaths e caminhos juntos na mesma lista de **TRANSformações** . Você não pode especificar as transformações de perfil e de segurança juntas na mesma lista. Você pode incluir transformações inseridas no pacote em uma lista com outras transformações.

``` syntax
@transform1.mst;:transform2.mst 
|\\server\share\path\transform1.mst;:transform2.mst
```

Observe que, como o delimitador de lista para transformações é o caractere ponto-e-vírgula, não deve ser usado em um nome de arquivo ou caminho de transformação.

## <a name="remarks"></a>Comentários

nos casos em que a [política TransformsSecure](transformssecure-policy.md) ou a propriedade [**TransformsSecure**](transformssecure.md) foi definida com Windows Installer, não é necessário passar o símbolo @ ou \| ao definir **transformações** usando a linha de comando. O instalador assume a segurança segura em código-fonte ou o caminho completo seguro se a lista consistir inteiramente de nomes de arquivos localizados na origem ou se consistir inteiramente em caminhos completos. Você ainda não pode misturar os dois tipos de fontes de transformação.

Observe que o instalador usa uma ordem de pesquisa diferente para transformações não seguras aplicadas durante as instalações pela primeira vez e manutenção. Para obter mais informações, consulte [transformações não seguras](unsecured-transforms.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador no Windows Server 2003 ou Windows XP. consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre o service pack mínimo Windows exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> <dt>

[Transformações de banco de dados](database-transforms.md)
</dt> <dt>

[Mesclagens e transformações](merges-and-transforms.md)
</dt> <dt>

[Resiliência de origem](source-resiliency.md)
</dt> </dl>

 

 




