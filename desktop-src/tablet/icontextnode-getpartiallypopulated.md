---
description: Recupera o valor que indica se um objeto IContextNode é parcialmente populado ou totalmente populado.
ms.assetid: 13ac3fb2-7baa-48d7-bf8e-f36b4031fbc4
title: Método IContextNode::GetPartiallyPopulated (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetPartiallyPopulated
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2fab5b5fce4d87c32fb3435fdad2cfc6b126069b40c7e5c7c2fb302ee468e480
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773796"
---
# <a name="icontextnodegetpartiallypopulated-method"></a>Método IContextNode::GetPartiallyPopulated

Recupera o valor que indica se um [**objeto IContextNode**](icontextnode.md) é parcialmente populado ou totalmente populado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetPartiallyPopulated(
  [out] VARIANT_BOOL *pfPartiallyPopulated
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pfPartiallyPopulated* \[ out\]
</dt> <dd>

**VARIANT \_ TRUE** se esse [**objeto IContextNode**](icontextnode.md) não contém dados completos; caso contrário, **VARIANT \_ FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para ver uma descrição dos valores de retorno, consulte [Classes e interfaces – Análise de Tinta.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentários

Use esse método quando seu aplicativo mantiver sua própria estrutura de dados, que é sincronizada com a do [**IInkAnalyzer.**](iinkanalyzer.md) Para obter mais informações, consulte [Proxy de dados com análise de tinta](data-proxy-with-ink-analysis.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>IACom.h (também requer IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IContextNode::SetPartiallyPopulated**](icontextnode-setpartiallypopulated.md)
</dt> <dt>

[**IContextNode::CreatePartiallyPopulatedSubNode**](icontextnode-createpartiallypopulatedsubnode.md)
</dt> <dt>

[**\_IAnalysisProxyEvents::P opulateContextNode**](-ianalysisproxyevents-populatecontextnode.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




