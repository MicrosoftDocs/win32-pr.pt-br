---
title: VBRPeak
description: O atributo VBRPeak contém a taxa de bits momentânea mais alta em um fluxo codificado de taxa de bits variável (VBR).
ms.assetid: 7b735145-8235-4efb-986f-952989b739bc
keywords:
- Formato de mídia do Windows VBRPeak
topic_type:
- apiref
api_name:
- VBRPeak
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af9163e64aa3d309af8fd35626b7a4c0397ba4c949213ef351c1ac73ee9575a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119704836"
---
# <a name="vbrpeak"></a>VBRPeak

O **atributo VBRPeak** contém a taxa de bits momentânea mais alta em um fluxo codificado de taxa de bits variável (VBR).

## <a name="global-constant"></a>Constante global

g \_ wszVBRPeak

## <a name="data-type"></a>Tipo de Dados

**WMT \_ TYPE \_ DWORD**

## <a name="remarks"></a>Comentários

Ao acessar a interface **IWMHeaderInfo3** do objeto writer, você pode adicionar ou alterar esse valor. Em outros objetos (editor de metadados, leitor e leitor síncrono), esse valor é somente leitura.

O autor grava automaticamente um **valor VBRPeak** para cada fluxo VBR.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lista de Atributos**](attribute-list.md)
</dt> </dl>

 

 




