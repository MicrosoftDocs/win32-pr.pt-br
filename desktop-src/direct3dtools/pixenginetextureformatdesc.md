---
description: Representa uma descrição de um formato de textura.
MS-HAID: vspixengine.PixEngineTextureFormatDesc
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Estrutura PixEngineTextureFormatDesc
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 685DC746-544D-4ACB-AB1F-9FA62C5CF416
api_name:
- PixEngineTextureFormatDesc
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 960186f0c28be88805c1df65f1a517c4ce4a4c64
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103919946"
---
# <a name="span-idvspixenginepixenginetextureformatdescspanpixenginetextureformatdesc-structure"></a><span id="vspixengine.pixenginetextureformatdesc"></span>Estrutura PixEngineTextureFormatDesc

Representa uma descrição de um formato de textura.

## <a name="syntax"></a>Sintaxe


```C++
} PixEngineTextureFormatDesc;
```

## <a name="members"></a>Membros

**dxgiFormat**  
O formato DXGI da textura.

**Formato de DataFormat**  
O formato de dados da textura.

**blockBytes**  
O número de bytes em um bloco de dados.

**blockHeight**  
A altura (exemplos de número no eixo Y) do bloco.

**blockWidth**  
A largura (número de amostras no eixo X) do bloco.

**channelX**  
Descreve as propriedades do canal X. Para obter mais informações, consulte a estrutura PixEngineChannelDescription.

**canal**  
Descreve as propriedades do canal Y. Para obter mais informações, consulte a estrutura PixEngineChannelDescription.

**channelZ**  
Descreve as propriedades do canal Z. Para obter mais informações, consulte a estrutura PixEngineChannelDescription.

**channelW**  
Descreve as propriedades do canal W. Para obter mais informações, consulte a estrutura PixEngineChannelDescription.

**swizzle**  
Descreve o swizzle (troca de canal) aplicado ao exemplo.

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>parâmetro</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



