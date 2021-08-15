---
description: A estrutura STATIONQUERY fornece informações sobre um computador específico usando Monitor de Rede.
ms.assetid: b7202c6b-e2b9-4a6f-8b87-3d11879f1d69
title: Estrutura STATIONQUERY (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STATIONQUERY
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: a2e46f4c0d213091a3915b5310d7768a193d33e5ac3391fd3bc3c6781e32cb57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118363052"
---
# <a name="stationquery-structure"></a>Estrutura STATIONQUERY

A estrutura **STATIONQUERY** fornece informações sobre um computador específico usando monitor de rede.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _STATIONQUERY {
  DWORD Flags;
  BYTE  BCDVerMinor;
  BYTE  BCDVerMajor;
  DWORD LicenseNumber;
  BYTE  MachineName[MACHINE_NAME_LENGTH];
  BYTE  UserName[USER_NAME_LENGTH];
  BYTE  Reserved[32];
  BYTE  AdapterAddress[6];
  WCHAR WMachineName[MACHINE_NAME_LENGTH];
  WCHAR WUserName[USER_NAME_LENGTH];
} STATIONQUERY, *LPSTATIONQUERY;
```



## <a name="members"></a>Membros

<dl> <dt>

**Sinalizadores**
</dt> <dd>

Sinalizadores que identificam o estado atual de Monitor de Rede.



| Valor                                                                                                                                                                                                                | Significado                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span id="STATIONQUERY_FLAGS_LOADED"></span><span id="stationquery_flags_loaded"></span><dl> <dt>**\_sinalizadores STATIONQUERY \_ carregados**</dt> </dl>                   | O driver está carregado, mas o kernel não é.<br/> |
| <span id="STATIONQUERY_FLAGS_RUNNING"></span><span id="stationquery_flags_running"></span><dl> <dt>**STATIONQUERY \_ sinalizadores \_ em execução**</dt> </dl>                | O driver está carregado, mas não está capturando dados.<br/> |
| <span id="STATIONQUERY_FLAGS_CAPTURING"></span><span id="stationquery_flags_capturing"></span><dl> <dt>**\_captura de sinalizadores STATIONQUERY \_**</dt> </dl>          | O driver está ativamente envolvido em uma captura.<br/> |
| <span id="STATIONQUERY_FLAGS_TRANSMITTING"></span><span id="stationquery_flags_transmitting"></span><dl> <dt>**STATIONQUERY \_ sinalizadores de \_ transmissão**</dt> </dl> | Esse sinalizador é obsoleto.<br/>                       |



 

</dd> <dt>

**BCDVerMinor**
</dt> <dd>

Número de versão secundária de Monitor de Rede instalado no computador.

</dd> <dt>

**BCDVerMajor**
</dt> <dd>

Número de versão principal do Monitor de Rede instalado no computador.

</dd> <dt>

**LicenseNumber**
</dt> <dd>

Número de licença do software.

</dd> <dt>

**MachineName**
</dt> <dd>

Nome do fabricante do computador, se houver.

</dd> <dt>

**UserName**
</dt> <dd>

Nome de usuário ou identificador do sistema.

</dd> <dt>

**Reserved**
</dt> <dd>

Reservado para uso futuro.

</dd> <dt>

**AdapterAddress**
</dt> <dd>

Endereço NIC.

</dd> <dt>

**WMachineName**
</dt> <dd>

Nome do computador Unicode. Este membro se aplica ao Monitor de Rede 2,0 ou posterior.

</dd> <dt>

**WUserName**
</dt> <dd>

Nome de usuário Unicode. Este membro se aplica ao Monitor de Rede 2,0 ou posterior.

</dd> </dl>

## <a name="remarks"></a>Comentários

Uma matriz dessas estruturas é usada pela estrutura de tabela de [consulta](querytable.md) para fornecer uma lista dos computadores que atualmente estão usando monitor de rede para capturar dados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[CONSULTA](querytable.md)
</dt> </dl>

 

 




