---
description: Representa informações sobre um arquivo de código-fonte.
MS-HAID: vspixengine.SourceFileInfo
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Estrutura SourceFileInfo
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A5222610-36ED-4F3B-BD95-A4F8611CC557
api_name:
- SourceFileInfo
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3e0528e61e830872a3e3b1c0555e541fc41d9d39
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456692"
---
# <a name="span-idvspixenginesourcefileinfospansourcefileinfo-structure"></a><span id="vspixengine.sourcefileinfo"></span>Estrutura SourceFileInfo

Representa informações sobre um arquivo de código-fonte.

## <a name="syntax"></a>Sintaxe


```C++
} SourceFileInfo;
```

## <a name="members"></a>Membros

**Nome do arquivo**  
Uma cadeia de caracteres COM comtaining o FilePath do arquivo de origem associado.

**checksumByteCount**  
O número de bytes na soma de verificação. Quando checkSumAlgorithm é igual a CHECKSUMALGORITHM:: MD5, checkSumByteCount é 16. Quando checkSumAlgorithm é igual a CHECKSUMALGORITHM:: SHA1, checkSumByteCount é 20.

**checkSumAlgorithm**  
Especifica o algoritmo usado para gerar a soma de verificação do arquivo. Os algoritmos com suporte são MD5 e SHA1. Para obter mais informações, consulte a enumeração CHECKSUMALGORITHM.

**checkSumFirstPart**  
A primeira parte de 8 bytes da soma de verificação.

**checkSumSecondPart**  
A segunda parte de 8 bytes da soma de verificação.

**checkSumThirdPart**  
A terceira parte de 8 bytes da soma de verificação.

**checkSumFourthPart**  
A quarta parte de 8 bytes da soma de verificação.

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>parâmetro</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



