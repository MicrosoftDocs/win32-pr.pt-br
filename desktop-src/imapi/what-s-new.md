---
title: O que há de novo (IMAPi)
description: A tabela a seguir identifica o que há de novo para cada versão da API de mestre de imagem.
ms.assetid: a90daec2-5916-4c24-b2ad-94199641a2ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77abc9db0c9d976eef632034a5620520bb29d73d
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "103640228"
---
# <a name="whats-new-image-mastering-api"></a>O que há de novo: API de mestre de imagem

A tabela a seguir identifica o que há de novo para cada versão da API de mestre de imagem.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Versão</th>
<th>Descrição dos recursos</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Versão 2,0</td>
<td>Grande parte da API foi reformulada. A maior parte da funcionalidade da versão 1,0 ainda está disponível na versão 2,0. Os aplicativos de escrita de mestre de imagem ou a execução de novos dispositivos e desenvolvimento de formato são incentivados a usar a versão 2,0 em vez da versão 1,0.<br/> O IMAPi 2,0 está incluído no Windows Vista. Habilitar a mesma funcionalidade para o Windows XP e o Windows Server 2003 requer a instalação do pacote de atualização do <a href="https://support.microsoft.com/kb/932716">KB932716</a> .<br/> Observações do Point-Release:<br/>
<ul>
<li>Uma atualização que oferece suporte a várias inicializações por meio da interface <a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage2"><strong>IFileSystemImage2</strong></a> foi introduzida no Windows Vista com Service Pack 1 (SP1) e Windows Server 2008.<br/></li>
<li>Uma atualização de recurso que oferece suporte a mestre para o formato BD-R\BD-RE, criação de imagem de disco bruto de CD em uma vez, bem como verificação de gravação foi incluída no <a href="https://www.microsoft.com/downloads/details.aspx?FamilyID=63ab51ea-99c9-45c0-980a-c556746fcf05">Feature Pack do Windows para armazenamento</a>. Essa atualização de recurso tem suporte no Windows Vista com SP1, no Windows XP com Service Pack 2 (SP2) e posterior e no Windows Server 2003 com Service Pack 1 (SP1) e posterior. Além disso, esses recursos estão incluídos no Windows 7 e no Windows Server 2008.<br/></li>
<li>Os recursos do IMAPi 2,0 nativos para o Windows 7 e o Windows Server 2008 incluem ' intervalo queimando ' para CDs de áudio e a eliminação de ' stash duplo ' durante operações de gravação. O stash duplo é um processo, dentro da maior operação de gravação, na qual cada arquivo é stash antes de ser gravado no disco. Com a versão mais recente do IMAPi 2,0, os arquivos são escolhidos seletivamente para o Stash, deixando os arquivos restantes (principalmente arquivos grandes) não-stash. O resultado final é o espaço em disco e a hora da operação salvos.<br/></li>
</ul></td>
</tr>
<tr class="even">
<td>Versão 1.0</td>
<td>Versão inicial. Permite que um aplicativo teste e grave uma imagem simples de áudio ou de dados em dispositivos CD-R e CD-RW. A API dá suporte ao formato Joliet e ISO 9660 para discos de dados e de áudio Redbook. Para obter informações sobre a versão 1,0, consulte <a href="imapiv1.md">suporte do IMAPIv1</a>. Incluído no Windows XP.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="version-20"></a>Versão 2,0

-   Permite que os aplicativos gravem nos formatos DVD-R, DVD + R, DVD-RW, DVD + RW, DVD + DL, DVD-DL e DVD-RAM, BD-R e BD-RE de mídia.
-   Permite a gravação em várias unidades ao mesmo tempo. Na versão 1,0, somente um gravador no sistema poderia ser usado pelo IMAPi ao mesmo tempo. Se você executar um aplicativo da versão 1,0 no Windows Vista, outros aplicativos poderão usar simultaneamente as interfaces IMAPi 1,0 ou 2,0 em outras unidades do sistema. Embora isso seja geralmente visto como um benefício, os aplicativos que se basearam no comportamento do gravador de sistema único podem exigir atualizações secundárias.
-   O acesso a um gravador é negado quando o gravador está gravando informações no disco. Caso contrário, o gravador estará disponível para outros clientes.
-   Dá suporte a mais de um arquivo stash em um computador cliente, enquanto a versão 1,0 permitia apenas um arquivo stash de todo o sistema.
-   No Windows Vista, a versão 1,0 não contém mais componentes de modo kernel ou serviço. No entanto, a interface [**IDiscRecorder2**](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2) ainda usa os \_ comandos de acesso exclusivo do CD-ROM do IOCTL \_ \_ e IOCTL \_ SCSI \_ \_ de passagem \_ para gerenciar o acesso ou a comunicação com dispositivos específicos da unidade.
-   No Windows Vista, as interfaces da versão 1,0 agora chamam as interfaces da versão 2,0.
-   Incluído no Windows Vista com SP1 e no Windows Server 2008, o IMAPi versão 2,0 oferece suporte à inicialização múltipla por meio da interface [**IFileSystemImage2**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage2) .
-   Permite o uso de ' intervalo Burning ' para CDs de áudio. Com a gravação intervalo, a lacuna audível entre faixas de áudio pode ser removida.
-   "Stash duplo" substituído por um processo que seleciona especificamente arquivos para o stash e deixa os arquivos restantes (principalmente arquivos grandes) não stash. O resultado final é o espaço em disco e a hora da operação salvos.
-   Com o [Windows Feature Pack para armazenamento](https://www.microsoft.com/downloads/details.aspx?FamilyID=63ab51ea-99c9-45c0-980a-c556746fcf05), as opções de verificação de gravação foram disponibilizadas com uma propriedade acessada por meio de [**IBurnVerification**](/windows/desktop/api/imapi2/nn-imapi2-iburnverification).
