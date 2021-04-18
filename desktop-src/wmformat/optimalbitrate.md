---
title: OptimalBitrate
description: O atributo OptimalBitrate contém a taxa de bits na qual o arquivo é melhor tocado.
ms.assetid: cd13b9b5-34d2-4ebb-9f10-3bf42dd9de81
keywords:
- Formato de mídia do Windows OptimalBitrate
topic_type:
- apiref
api_name:
- OptimalBitrate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff71c6b64cbc4bf4ccc4f346e62a5eae066e78ce
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105782723"
---
# <a name="optimalbitrate"></a>OptimalBitrate

O atributo **OptimalBitrate** contém a taxa de bits na qual o arquivo é melhor tocado.

## <a name="global-constant"></a>Constante global

g \_ wszWMOptimalBitrate

## <a name="data-type"></a>Tipo de Dados

**WMT \_ tipo \_ DWORD**

## <a name="remarks"></a>Comentários

Este é um atributo codificado.

Para arquivos que contêm fluxos de taxa de bits variável (VBR), esse valor é a taxa de bits de pico para os fluxos no arquivo. Para arquivos sem VBR, esse valor é o mesmo que [**taxa de bits**](bit-rate.md).

Este atributo não pode ser duplicado no nível do arquivo. Se esse atributo for usado para um fluxo individual, ele será tratado como metadados personalizados e não transmitirá seu significado normal para os objetos do SDK do Windows Media Format.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lista de Atributos**](attribute-list.md)
</dt> </dl>

 

 




