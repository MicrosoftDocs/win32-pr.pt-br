---
title: External. viewparameters
description: Observação Este tópico descreve a funcionalidade projetada para uso por lojas online. | External. viewparameters
ms.assetid: 0afabe35-2857-413a-a662-1a76d3fb75fe
keywords:
- Windows Media Player external. viewparameters
topic_type:
- apiref
api_name:
- External.viewParameters
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7df2d19998610ca552e06f63a348d9d794bfc471c766f8603f01398026422d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118837747"
---
# <a name="externalviewparameters"></a>External. viewparameters

> [!Note]  
> Este tópico descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

A propriedade **viewparameters** recupera parâmetros associados à exibição atual no Windows Media Player.

## <a name="syntax"></a>Syntax

**janela. external. viewparameters**

## <a name="possible-values"></a>Valores possíveis

Essa propriedade retorna uma **cadeia de caracteres** somente leitura.

## <a name="remarks"></a>Comentários

Essa propriedade recupera parâmetros que foram definidos anteriormente pela loja online. Por exemplo, a loja online pode especificar parâmetros de exibição no parâmetro *ViewParams* do método [changeView](external-changeview.md) ou o parâmetro *params* do método [changeViewOnlineList](external-changeviewonlinelist.md) .

Os parâmetros de exibição não são interpretados pelo Windows Media Player. Eles são criados pela loja online e têm significado apenas para a loja online.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto externo para repositórios online do tipo 1**](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





