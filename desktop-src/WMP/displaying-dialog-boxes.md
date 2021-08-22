---
title: Exibindo caixas de diálogo
description: Exibindo caixas de diálogo
ms.assetid: 637555af-0a36-4aee-908f-496b52f7bd78
keywords:
- Windows Media Player lojas online, exibindo caixas de diálogo
- lojas online, exibindo caixas de diálogo
- tipo 1 lojas online, exibindo caixas de diálogo
- Windows Media Player lojas online, caixas de diálogo
- lojas online, caixas de diálogo
- tipos 1 lojas online, caixas de diálogo
- exibindo caixas de diálogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00e71d177e7675822b1f2704bf62776e598c2e817d583020b0df962347dac4f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997266"
---
# <a name="displaying-dialog-boxes"></a>Exibindo caixas de diálogo

A loja online pode invocar caixas de diálogo por meio de Windows Media Player. Para fazer isso, chame [external. ShowPopup](external-showpopup.md) do código de script da página de descoberta, fornecendo um valor de índice personalizado que representa a caixa de diálogo a ser exibida. Esse valor de índice tem significado apenas para o código da loja online; Windows Media Player não interpreta esse valor. em seguida, Windows Media Player chama [IWMPContentPartner:: GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo), passando g \_ szItemInfo \_ PopupURL para o parâmetro *bstrInfoName* e o número de índice para o parâmetro *pContext* . Em seguida, o plug-in retorna um **BSTR** contendo a URL da página da Web a ser exibida na caixa de diálogo e o Player mostra a caixa de diálogo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Guia de programação para lojas online do tipo 1**](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




