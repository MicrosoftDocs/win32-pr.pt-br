---
title: Taxa de trabalho ideal
description: O atributo OptimalBitrate contém a taxa de bits na qual o arquivo é melhor interpretado.
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
ms.openlocfilehash: 5f670c2acd2f2190a5ee2bfd76994c219c6f967dbbd933520a8d4627236a0d36
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930626"
---
# <a name="optimalbitrate"></a>Taxa de trabalho ideal

O **atributo OptimalBitrate** contém a taxa de bits na qual o arquivo é melhor interpretado.

## <a name="global-constant"></a>Constante global

g \_ wszWMOptimalBitrate

## <a name="data-type"></a>Tipo de Dados

**WMT \_ TYPE \_ DWORD**

## <a name="remarks"></a>Comentários

Esse é um atributo codificado.

Para arquivos que contêm fluxos de VBR (taxa de bits variável), esse valor é a taxa de bits de pico para os fluxos no arquivo. Para arquivos sem VBR, esse valor é o mesmo que [**Taxa de bits.**](bit-rate.md)

Esse atributo não pode ser duplicado no nível do arquivo. Se esse atributo for usado para um fluxo individual, ele será tratado como metadados personalizados e não transmitirá seu significado normal para os objetos do SDK Windows Formato de Mídia.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lista de Atributos**](attribute-list.md)
</dt> </dl>

 

 




