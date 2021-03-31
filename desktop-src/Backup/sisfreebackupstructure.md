---
title: Função SisFreeBackupStructure (Sisbkup. h)
description: Libera a estrutura de backup do SIS especificada.
ms.assetid: 34d5e919-e4bf-4105-ac15-a2ff5adfbdee
keywords:
- Backup de função SisFreeBackupStructure
topic_type:
- apiref
api_name:
- SisFreeBackupStructure
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3a135c4787ff116ec10efd61fa1492033393c88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644448"
---
# <a name="sisfreebackupstructure-function"></a>Função SisFreeBackupStructure

A função **SisFreeBackupStructure** libera a estrutura de backup do SIS especificada.

## <a name="syntax"></a>Sintaxe


```C++
BOOL SisFreeBackupStructure(
  _In_ PVOID sisBackupStructure
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sisBackupStructure* \[ no\]
</dt> <dd>

Ponteiro para a estrutura de backup do SIS retornada de [**SisCreateBackupStructure**](siscreatebackupstructure.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função retornará **true** se for concluída com êxito e **false** caso contrário. Chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obter mais informações sobre o motivo da falha na chamada.

## <a name="remarks"></a>Comentários

Essa função deve ser chamada depois que a operação de backup for concluída para o volume identificado pelo valor do parâmetro *sisBackupStructure* .

Observe que não é seguro pressupor que isso apenas desaloque memória. Por exemplo, essa função também pode executar operações administrativas adicionais para a arquitetura do SIS. Portanto, chame essa função mesmo que sua operação de backup seja encerrada imediatamente depois.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                   |
| parâmetro<br/>                   | <dl> <dt>Sisbkup. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Sisbkup. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Sisbkup.dll</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**SisCreateBackupStructure**](siscreatebackupstructure.md)
</dt> </dl>

 

