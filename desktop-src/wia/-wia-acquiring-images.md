---
description: Depois que uma imagem tiver sido selecionada, um aplicativo usará a interface IWiaDataTransfer (para aplicativos executados no Windows XP ou anterior) ou a interface IWiaTransfer (para aplicativos executados no Windows Vista ou posterior) para transferir dados de imagem de dispositivos de geração de imagens. Consulte transferência de dados de imagem no WIA 1,0 ou transferência de dados de imagem no WIA 2,0 para obter detalhes.
ms.assetid: cf76e526-d63b-4ee5-ba3c-871f2051a82c
title: Adquirindo imagens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d062cb370327311ad0c7d4f883344c05bb776f6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813359"
---
# <a name="acquiring-images"></a>Adquirindo imagens

Depois que uma imagem tiver sido selecionada, um aplicativo usará a interface [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) (para aplicativos executados no Windows XP ou anterior) ou a interface [**IWiaTransfer**](-wia-iwiatransfer.md) (para aplicativos executados no Windows Vista ou posterior) para transferir dados de imagem de dispositivos de geração de imagens. Consulte [transferência de dados de imagem no wia 1,0](-wia-transferring-image-data.md) ou [transferência de dados de imagem no WIA 2,0](-wia-transferring-image-data-in-wia2.md) para obter detalhes.

Depois que um dispositivo tiver sido selecionado, um aplicativo usará o método [**IWiaItem::D evicedlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-devicedlg) da interface [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) ou [**IWiaItem2**](-wia-iwiaitem2.md) do dispositivo (o item raiz) para selecionar uma imagem de um dispositivo de aquisição de imagem do Windows (WIA) especificado. O método [**IWiaDevMgr:: GetImageDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-getimagedlg) exibe uma caixa de diálogo que permite que um usuário selecione uma imagem de um dispositivo especificado e transfere a imagem para um nome de arquivo selecionado pelo usuário. Ele também permite que o usuário especifique um dispositivo, se necessário. Para obter mais informações, consulte [selecionando um dispositivo](-wia-selecting-a-device.md)

Observe que não é necessário que um usuário selecione uma imagem usando o método acima. Um aplicativo pode obter um ponteiro para um item de imagem diretamente da árvore de itens de um dispositivo. Para obter instruções, consulte [navegando em uma árvore de itens](-wia-navigating-an-item-tree.md).

Depois que o item WIA que representa a imagem desejada tiver sido selecionado, um aplicativo em execução no Windows XP ou anterior consultará a interface [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) desse item para um ponteiro para sua interface [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) . Um aplicativo em execução no Windows Vista ou posterior consulta a interface [**IWiaItem2**](-wia-iwiaitem2.md) para um ponteiro para sua interface [**IWiaTransfer**](-wia-iwiatransfer.md) .

O aplicativo pode então usar os métodos da interface [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) (ou [**IWiaTransfer**](-wia-iwiatransfer.md)) para transferir os dados da imagem para o aplicativo.

Se o dispositivo de geração de imagens for um scanner, [**IWiaDataTransfer:: idtGetData**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtgetdata)ou outros métodos da interface [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) , o disparará uma operação de verificação e, em seguida, transferirá os dados de imagem resultantes. Se o dispositivo for uma câmera, os dados da imagem serão simplesmente transferidos da câmera para o aplicativo.

 

 



