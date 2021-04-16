---
description: A estrutura EXPERTCONFIG contém os dados de configuração do especialista. O especialista sobrepõe o membro RawConfigData com uma estrutura específica de especialista.
ms.assetid: 6167e846-d58c-40a8-94f7-c6d6185ae724
title: Estrutura EXPERTCONFIG (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERTCONFIG
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 293bdf4c792c10232564a7ba6386df430e81ecb5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758295"
---
# <a name="expertconfig-structure"></a>Estrutura EXPERTCONFIG

A estrutura **EXPERTCONFIG** contém os dados de configuração do especialista. O especialista sobrepõe o membro **RawConfigData** com uma estrutura específica de especialista.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  DWORD RawConfigLength;
  BYTE  RawConfigData[];
} EXPERTCONFIG, *PEXPERTCONFIG;
```



## <a name="members"></a>Membros

<dl> <dt>

**RawConfigLength**
</dt> <dd>

Comprimento total da estrutura, incluindo os quatro bytes usados para o membro. Monitor de Rede usa o valor quando a estrutura é salva e lida a partir de uma unidade de disco.

</dd> <dt>

**RawConfigData**
</dt> <dd>

Dados de configuração. O especialista deve adicionar os dados de configuração. Por exemplo, suponha que você tenha uma estrutura de dados parecida com esta.

``` syntax
typedef struct
{
    DWORD       RawConfigLength;   // Overlay of structure
    DWORD       PickNumEvents;
    DWORD       NumEventsSpecific;
    DWORD       PickSpeedThroughCapture;
    DWORD       PickStartup;
    DWORD       PickAttachProperties;
} TESTEXPERTCONFIG;
typedef TESTEXPERTCONFIG* LPTESTEXPERTCONFIG;
```

Observe que o **RawConfigLength** garante que a sobreposição funcione corretamente. Quando você usa os dados, seu código pode ter a seguinte aparência:

``` syntax
BOOL WINAPI Configure( 
    HEXPERTKEY ExpertKey,
    PEXPERTCONFIG * ppConfig,
    PEXPERTSTARTUPINFO pStartupInfo,
    DWORD StartupFlags,
    HWND hWnd
)
{
    LPTESTEXPERTCONFIG  lpConfig;

    //...
    lpConfig = (LPTESTEXPERTCONFIG)(*ppConfig);
    //...
}
```

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




