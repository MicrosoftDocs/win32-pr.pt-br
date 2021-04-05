---
description: O CABINETDLLVERSIONINFO contém as informações de versão para Cabinet.dll.
ms.assetid: 1dc6962c-3087-4f56-8b65-fbf55e17eeb6
title: Estrutura CABINETDLLVERSIONINFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CABINETDLLVERSIONINFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: b6dfcd68f1bc684554d45feb13b9976465b70efa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826334"
---
# <a name="cabinetdllversioninfo-structure"></a>Estrutura CABINETDLLVERSIONINFO

\[Esta estrutura contém informações necessárias apenas ao usar a função **DllGetVersion** , que não tem suporte. Esta documentação é fornecida apenas para fins informativos.\]

O **CABINETDLLVERSIONINFO** contém as informações de versão para Cabinet.dll.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  DWORD cbStruct;
  DWORD dwReserved1;
  DWORD dwReserved2;
  DWORD dwFileVersionMS;
  DWORD dwFileVersionLS;
} CABINETDLLVERSIONINFO, *PCABINETDLLVERSIONINFO;
```



## <a name="members"></a>Membros

<dl> <dt>

**cbStruct**
</dt> <dd>

O tamanho dessa estrutura, em bytes.

</dd> <dt>

**dwReserved1**
</dt> <dd>

Reservado.

</dd> <dt>

**dwReserved2**
</dt> <dd>

Reservado.

</dd> <dt>

**dwFileVersionMS**
</dt> <dd>

Contém os bits mais significativos das informações de versão. O bits 0-15 contém a versão secundária e o bits 16-31 contém a versão principal.

</dd> <dt>

**dwFileVersionLS**
</dt> <dd>

Contém os bits menos significativos das informações de versão. O bits 0-15 contém o número de revisão e o bits 16-31 contém o número de Build.

</dd> </dl>

## <a name="see-also"></a>Confira também

<dl> <dt>

[**DllGetVersion**](dllgetversion.md)
</dt> </dl>

 

 



