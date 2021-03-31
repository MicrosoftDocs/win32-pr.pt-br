---
title: Estrutura de MPCLEAN_DATA (MpClient. h)
description: Dados de notificação passados para a função de retorno de chamada limpa.
ms.assetid: 475A6525-5BD8-4B29-A684-53EE2758C790
keywords:
- Recursos do ambiente Windows herdado da estrutura de MPCLEAN_DATA
- Ponteiro de estrutura de PMPCLEAN_DATA recursos de ambiente herdados do Windows
topic_type:
- apiref
api_name:
- MPCLEAN_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89f0c7e867918b6567279be7c41ce72e7e396576
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644531"
---
# <a name="mpclean_data-structure"></a>\_Estrutura de dados MPCLEAN

Dados de notificação passados para a função de retorno de chamada limpa.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct tagMPCLEAN_DATA {
  MPTHREAT_ID      ThreatID;
  MPTHREAT_ACTION  ThreatAction;
  DWORD            dwStatus;
  PMPRESOURCE_INFO ResourceInfo;
} MPCLEAN_DATA, *PMPCLEAN_DATA;
```



## <a name="members"></a>Membros

<dl> <dt>

**Threatid**
</dt> <dd>

Tipo: **\_ ID de MPTHREAT**

</dd> <dd>

Identificador de ameaça para o **mpnotify \_ limpar \_ ameaça \_ Iniciar** / **mpnotify limpeza de ameaça \_ \_ \_ bem-sucedida** / **mpnotify eventos \_ \_ \_ com falha de limpeza de ameaça** . O bit superior é definido para identificar ameaças relacionadas ao antivírus.

</dd> <dt>

**Threataction**
</dt> <dd>

Tipo: **[ **\_ ação MPTHREAT**](mpthreat-action.md)**

</dd> <dd>

Ação de ameaça para o **mpnotify \_ limpar \_ ameaça \_ Iniciar** / **mpnotify limpeza de ameaça \_ \_ \_ bem-sucedida** / **mpnotify eventos \_ \_ \_ com falha de limpeza de ameaça** . Consulte [**a \_ ação MPTHREAT**](mpthreat-action.md).

</dd> <dt>

**dwStatus**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Status ou ações adicionais associadas à ação executada. Essa é uma combinação de sinalizadores de bit [**do \_ sinalizador MPSTATUS**](mpstatus-flag.md).

</dd> <dt>

**ResourceInfo**
</dt> <dd>

Tipo: **\_ informações de PMPRESOURCE**

</dd> <dd>

Informações de recurso para a **mpnotify \_ limpeza de \_ ameaça \_ Iniciar** / **mpnotify limpeza de ameaça \_ \_ \_ bem-sucedida** / **mpnotify eventos \_ \_ \_ com falha de limpeza de ameaça** . Consulte [**MPRESOURCE \_ info**](mpresource-info.md).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**informações de MPRESOURCE \_**](mpresource-info.md)
</dt> <dt>

[**\_sinalizador MPSTATUS**](mpstatus-flag.md)
</dt> <dt>

[**\_ação MPTHREAT**](mpthreat-action.md)
</dt> </dl>

 

 





