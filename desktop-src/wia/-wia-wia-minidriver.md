---
description: Os aplicativos veem os dispositivos de aquisição de imagem do Windows (WIA) como uma árvore hierárquica de objetos IWiaItem ou IWiaItem2 com o item raiz que representa o próprio dispositivo.
ms.assetid: ae4ded93-09be-4caa-ad6e-1a9071fdb4b6
title: Minidriver WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5aadaf55cfe2e8102d4e0e02cf9787b9696e327
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501775"
---
# <a name="wia-minidriver"></a>Minidriver WIA

Os aplicativos veem os dispositivos de aquisição de imagem do Windows (WIA) como uma árvore hierárquica de objetos [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) ou [**IWiaItem2**](-wia-iwiaitem2.md) com o item raiz que representa o próprio dispositivo. Os dispositivos WIA podem ser usados simultaneamente por mais de um aplicativo. Portanto, é necessário que a exibição de cada aplicativo de um objeto **IWiaItem** ou **IWiaItem2** seja independente das exibições de outro aplicativo. Isso é feito com dois objetos de item diferentes. O driver cria a árvore de itens de driver de objetos de [interface IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) , também chamados de itens de driver, usando os métodos de serviços de driver WIA. Esses são objetos globais que o driver usa para representar os itens internos de cada driver. Quando um aplicativo cria um objeto **IWiaItem** ou **IWiaItem2** (também chamado de item de aplicativo), esse objeto é vinculado à [interface IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) correspondente do driver na árvore de itens de driver. Uma contagem de referência é mantida no objeto de [interface IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) sujeito às seguintes regras:

-   Quando um driver adiciona um objeto de [interface IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) à árvore de itens de driver, a contagem de referência do objeto de [interface IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) é incrementada. Normalmente, isso ocorre durante o [IWiaMiniDrv::D rvinitializewia](https://msdn.microsoft.com/library/ms794097.aspx) ou quando um \_ comando de sincronização de cmd WIA \_ é processado.
-   Quando um driver remove um objeto de [interface IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) da árvore de itens de driver, a contagem de referência do objeto de [interface IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) é decrementada e o objeto de [interface IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) é marcado para que ele não possa acessar o dispositivo novamente. Normalmente, isso ocorre quando um dispositivo é desconectado ou um item é excluído. Os aplicativos ainda podem ler propriedades de um objeto [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) ou [**IWiaItem2**](-wia-iwiaitem2.md) mesmo quando o objeto de [interface IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) correspondente foi removido da árvore de itens de driver.
-   Quando um objeto [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) ou [**IWiaItem2**](-wia-iwiaitem2.md) é criado, ele é vinculado a um objeto de [interface IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) correspondente. A contagem de referência do objeto de [interface IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) é incrementada.
-   Quando um objeto [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) ou [**IWiaItem2**](-wia-iwiaitem2.md) é liberado, o link para seu objeto de [interface IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) correspondente é grave e a contagem de referência do objeto de [interface IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) é diminuída.
-   Se a contagem de referência de um objeto de [interface IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) chegar a zero, o objeto de [interface IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) será excluído. Isso se aplica a todos os objetos de [interface IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) , incluindo o item raiz. A contagem de referência de um objeto de [interface IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) só vai para zero quando nenhum item de aplicativo faz referência a ele e não está mais vinculado à árvore de itens de driver.

Usando esse esquema de contagem de referência, muitos objetos [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) ou [**IWiaItem2**](-wia-iwiaitem2.md) podem ser vinculados a uma [interface IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) sem interferência. Como cada **IWiaItem** ou **IWiaItem2** contém seu próprio armazenamento de propriedade, um aplicativo pode continuar a ler as propriedades do item mesmo depois que um item tiver sido excluído, mas nenhuma operação que requer acesso ao dispositivo terá sucesso. Como as propriedades de item são armazenadas no objeto **IWiaItem** ou **IWiaItem2** , o driver deve definir as propriedades do objeto **IWiaItem** ou **IWiaItem2** para o dispositivo antes de uma transferência de dados.

 

 



