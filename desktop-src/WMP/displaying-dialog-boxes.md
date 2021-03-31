---
title: Exibindo caixas de diálogo
description: Exibindo caixas de diálogo
ms.assetid: 637555af-0a36-4aee-908f-496b52f7bd78
keywords:
- Lojas online do Windows Media Player, exibindo caixas de diálogo
- lojas online, exibindo caixas de diálogo
- tipo 1 lojas online, exibindo caixas de diálogo
- Lojas online do Windows Media Player, caixas de diálogo
- lojas online, caixas de diálogo
- tipos 1 lojas online, caixas de diálogo
- exibindo caixas de diálogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ebe008a6c3eac872edea497dc9d50da408aa7eb
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103640149"
---
# <a name="displaying-dialog-boxes"></a>Exibindo caixas de diálogo

A loja online pode invocar caixas de diálogo por meio do Windows Media Player. Para fazer isso, chame [external. ShowPopup](external-showpopup.md) do código de script da página de descoberta, fornecendo um valor de índice personalizado que representa a caixa de diálogo a ser exibida. Esse valor de índice tem significado apenas para o código da loja online; O Windows Media Player não interpreta esse valor. Em seguida, o Windows Media Player chama [IWMPContentPartner:: GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo), passando g \_ szItemInfo \_ PopupURL para o parâmetro *bstrInfoName* e o número de índice para o parâmetro *pContext* . Em seguida, o plug-in retorna um **BSTR** contendo a URL da página da Web a ser exibida na caixa de diálogo e o Player mostra a caixa de diálogo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Guia de programação para lojas online do tipo 1**](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




