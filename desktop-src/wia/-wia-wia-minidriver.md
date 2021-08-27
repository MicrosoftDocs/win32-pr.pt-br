---
description: Os aplicativos Windows wia (aquisição de imagem) como uma árvore hierárquica de objetos IWiaItem ou IWiaItem2 com o item raiz que representa o próprio dispositivo.
ms.assetid: ae4ded93-09be-4caa-ad6e-1a9071fdb4b6
title: WIA Minidriver
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37e8d3c520106c345bd02df5b686bb1abf34f9ff1aa0b338e645b178cabbb874
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056916"
---
# <a name="wia-minidriver"></a>WIA Minidriver

Os aplicativos Windows wia (aquisição de imagem) como uma árvore hierárquica de objetos [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) ou [**IWiaItem2**](-wia-iwiaitem2.md) com o item raiz que representa o próprio dispositivo. Dispositivos WIA podem ser usados simultaneamente por mais de um aplicativo. Portanto, é necessário que a exibição de cada aplicativo de um **objeto IWiaItem** ou **IWiaItem2** seja independente das exibições de outro aplicativo. Isso é feito com dois objetos de item diferentes. O driver cria a árvore de itens de driver de objetos da [Interface IWiaDrvItem,](https://msdn.microsoft.com/library/ms793976.aspx) também chamados de itens de driver, usando os métodos de serviços de driver WIA. Esses são objetos globais que o driver usa para representar os itens internos de cada driver. Quando um aplicativo cria um objeto **IWiaItem** ou **IWiaItem2** (também chamado de item de aplicativo), esse objeto é vinculado à [Interface IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) correspondente do driver na árvore de itens do driver. Uma contagem de referência é mantida no objeto [interface IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) sujeito às seguintes regras:

-   Quando um driver adiciona um objeto [interface IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) à árvore de itens do driver, a contagem de referência do objeto [interface IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) é incrementada. Isso normalmente ocorre durante [IWiaMiniDrv::d rvInitializeWia](https://msdn.microsoft.com/library/ms794097.aspx) ou quando um comando \_ WIA CMD \_ SYNCHRONIZE é processado.
-   Quando um driver remove um objeto interface [IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) da árvore de itens do driver, a contagem de referência do objeto da [Interface IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) é decrementada e o objeto [interface IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) é marcado para que ele não possa acessar o dispositivo novamente. Isso normalmente ocorre quando um dispositivo é desconectado ou um item é excluído. Os aplicativos ainda podem ler propriedades de um objeto [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) ou [**IWiaItem2**](-wia-iwiaitem2.md) mesmo quando o objeto de [Interface IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) correspondente tiver sido removido da árvore de itens do driver.
-   Quando um [**objeto IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) ou [**IWiaItem2**](-wia-iwiaitem2.md) é criado, ele é vinculado a um objeto [de Interface IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) correspondente. A contagem de referência do [objeto interface IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) é incrementada.
-   Quando um objeto [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) ou [**IWiaItem2**](-wia-iwiaitem2.md) é liberado, o link para seu objeto [de Interface IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) correspondente é cortado e a contagem de referência do objeto da [Interface IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) é decrementada.
-   Se a contagem de referência de um objeto [IWiaDrvItem Interface](https://msdn.microsoft.com/library/ms793976.aspx) for zero, o objeto [interface IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) será excluído. Isso se aplica a todos os [objetos da Interface IWiaDrvItem,](https://msdn.microsoft.com/library/ms793976.aspx) incluindo o item raiz. A contagem de referência de um objeto [da Interface IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) só vai para zero quando nenhum item de aplicativo faz referência a ele e não está mais vinculado à árvore de itens do driver.

Usando esse esquema de contagem de referência, muitos [**objetos IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) ou [**IWiaItem2**](-wia-iwiaitem2.md) podem ser vinculados a uma [interface IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) sem interferência. Como cada **IWiaItem** ou **IWiaItem2** contém seu próprio armazenamento de propriedades, um aplicativo pode continuar a ler as propriedades do item mesmo depois que um item tiver sido excluído, mas nenhuma operação que exija acesso ao dispositivo terá êxito. Como as propriedades do item são armazenadas no objeto **IWiaItem** ou **IWiaItem2,** o driver deve definir as propriedades do objeto **IWiaItem** ou **IWiaItem2** para o dispositivo antes de uma transferência de dados.

 

 



