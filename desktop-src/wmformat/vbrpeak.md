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
ms.openlocfilehash: 6e8aacb076c3e92cfa676e73e945506cc4942bf4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104006636"
---
# <a name="vbrpeak"></a>VBRPeak

O atributo **VBRPeak** contém a taxa de bits momentânea mais alta em um fluxo codificado de taxa de bits variável (VBR).

## <a name="global-constant"></a>Constante global

g \_ wszVBRPeak

## <a name="data-type"></a>Tipo de Dados

**WMT \_ tipo \_ DWORD**

## <a name="remarks"></a>Comentários

Ao acessar a interface **IWMHeaderInfo3** do objeto gravador, você pode adicionar ou alterar esse valor. Em outros objetos (editor de metadados, leitor e leitor síncrono), esse valor é somente leitura.

O gravador grava automaticamente um valor de **VBRPeak** para cada fluxo de VBR.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lista de Atributos**](attribute-list.md)
</dt> </dl>

 

 




