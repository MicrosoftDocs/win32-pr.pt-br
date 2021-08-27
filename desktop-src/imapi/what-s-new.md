---
title: Novidades (IMAPI)
description: A tabela a seguir identifica o que há de novo para cada versão da API de Controle de Imagem.
ms.assetid: a90daec2-5916-4c24-b2ad-94199641a2ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72a3b0ceb966f3f6db6583b86b616608da3bee4f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472172"
---
# <a name="whats-new-image-mastering-api"></a>Novidades: API de Mastering de Imagem

A tabela a seguir identifica o que há de novo para cada versão da API de Controle de Imagem.




| Versão | Descrição dos recursos | 
|---------|-------------------------|
| Versão 2,0 | Grande parte da API foi reprojetada. A maior parte da funcionalidade da versão 1.0 ainda está disponível na versão 2.0. Aqueles que escrevem aplicativos de mestre de imagem ou executam novos dispositivos e desenvolvimento de formato são incentivados a usar a versão 2.0 em vez da versão 1.0.<br /> O IMAPI 2.0 está incluído no Windows Vista. A habilitação da mesma funcionalidade para Windows XP e Windows Server 2003 requer a instalação do pacote de atualização <a href="https://support.microsoft.com/kb/932716">KB932716.</a><br /> Point-Release:<br /><ul><li>Uma atualização que oferece suporte a várias inicializações por meio da interface <a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage2"><strong>IFileSystemImage2</strong></a> foi introduzida no Windows Vista com Service Pack 1 (SP1) e Windows Server 2008.<br /></li><li>Uma atualização de recursos que oferece suporte de mastering para o formato BD-R\BD-RE, criação de imagem raw CD Disc-at-Once, bem como verificação de gravação foi incluída no <a href="https://www.microsoft.com/downloads/details.aspx?FamilyID=63ab51ea-99c9-45c0-980a-c556746fcf05">Feature Pack</a>do Windows para Armazenamento . Essa atualização de recurso tem suporte no Windows Vista com SP1, Windows XP com Service Pack 2 (SP2) e posterior e Windows Server 2003 com Service Pack 1 (SP1) e posterior. Além disso, esses recursos estão incluídos no Windows 7 e Windows Server 2008.<br /></li><li>Os recursos do IMAPI 2.0 nativos do Windows 7 e do Windows Server 2008 incluem "Gravação sem intervalo" para cds de áudio e a eliminação de "Double Stashing" durante operações de gravação. O stashing duplo é um processo, dentro da operação de burn maior, em que cada arquivo é feito antes de ser rebaixado para o disco. Com a versão mais recente do IMAPI 2.0, os arquivos são escolhidos seletivamente para o stashing, deixando os arquivos restantes (principalmente arquivos grandes) sem stash. O resultado final é espaço em disco salvo e tempo de operação.<br /></li></ul> | 
| Versão 1.0 | Versão inicial. Permite que um aplicativo seja estágio e queimem uma imagem de áudio ou dados simples em dispositivos CD-R e CD-RW. A API dá suporte aos formatos Det e ISO 9660 para discos de dados e áudio do Redbook. Para obter informações sobre a versão 1.0, consulte <a href="imapiv1.md">Suporte a IMAPIv1.</a> Incluído no Windows XP.<br /> | 




 

## <a name="version-20"></a>Versão 2,0

-   Permite que os aplicativos gravarem nos formatos de mídia DVD-R, DVD+R, DVD-RW, DVD+DL, DVD-DL e DVD-RAM, BD-R e BD-RE.
-   Permite a gravação em várias unidades ao mesmo tempo. Na versão 1.0, apenas um gravador no sistema pode ser usado pelo IMAPI ao mesmo tempo. Se você executar um aplicativo da versão 1.0 no Windows Vista, outros aplicativos poderão usar simultaneamente interfaces IMAPI 1.0 ou 2.0 em outras unidades no sistema. Embora isso geralmente seja visto como um benefício, os aplicativos que dependia do comportamento de comportamento de comportamento único do sistema podem exigir atualizações secundárias.
-   O acesso a um gravador é negado quando o gravador está escrevendo informações no disco. Caso contrário, o gravador estará disponível para outros clientes.
-   Dá suporte a mais de um arquivo de stash em um computador cliente, enquanto a versão 1.0 permitia apenas um arquivo de stash em todo o sistema.
-   No Windows Vista, a versão 1.0 não contém mais componentes de modo kernel ou serviço. No entanto, a interface [**IDiscRecorder2**](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2) ainda usa os comandos IOCTL CDROM EXCLUSIVE ACCESS e \_ \_ \_ IOCTL \_ SCSI PASS THROUGH DIRECT para gerenciar o acesso ou a comunicação com dispositivos de unidade \_ \_ \_ específicos.
-   No Windows Vista, as interfaces da versão 1.0 agora chamam as interfaces da versão 2.0.
-   Incluído no Windows Vista com SP1 e Windows Server 2008, o IMAPI vesion 2.0 oferece suporte multiboot por meio da interface [**IFileSystemImage2.**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage2)
-   Permite o uso de 'Gravação sem intervalo' para CDs de áudio. Com a Gravação Sem Intervalo, a lacuna audível entre faixas de áudio pode ser removida.
-   Substituiu 'Stashing Duplo' por um processo que seleciona especificamente arquivos para o stashing e deixa os arquivos restantes (principalmente arquivos grandes) não armazenados. O resultado final é espaço em disco salvo e tempo de operação.
-   Com o [Windows Feature Pack](https://www.microsoft.com/downloads/details.aspx?FamilyID=63ab51ea-99c9-45c0-980a-c556746fcf05)para Armazenamento , as opções de verificação de burn foram disponibilizadas com uma propriedade acessada por meio de I [**BeatVerification**](/windows/desktop/api/imapi2/nn-imapi2-iburnverification).
