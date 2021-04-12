---
title: Função SisFreeRestoreStructure (Sisbkup. h)
description: Libera a memória alocada para a estrutura de restauração do SIS especificada e executa tarefas que preparam o filtro SIS para configurar corretamente os links criados durante a operação de restauração.
ms.assetid: dbdccb53-b38e-465d-a6d0-ee86923a5879
keywords:
- Backup de função SisFreeRestoreStructure
topic_type:
- apiref
api_name:
- SisFreeRestoreStructure
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7293514d798fe65c82863a83549039b05ec8eb3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455817"
---
# <a name="sisfreerestorestructure-function"></a>Função SisFreeRestoreStructure

A função **SisFreeRestoreStructure** libera a memória alocada para a estrutura de restauração do SIS especificada e executa tarefas que preparam o filtro SIS para configurar corretamente os links criados durante a operação de restauração.

## <a name="syntax"></a>Sintaxe


```C++
BOOL SisFreeRestoreStructure(
  _In_ PVOID sisRestoreStructure
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sisRestoreStructure* \[ no\]
</dt> <dd>

Ponteiro para uma estrutura de restauração do SIS retornada de [**SisCreateRestoreStructure**](siscreaterestorestructure.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função retornará **true** se for concluída com êxito e **false** caso contrário. Chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obter mais informações sobre o motivo da falha na chamada.

## <a name="remarks"></a>Comentários

Acessar os links do SIS antes que a chamada para essa função seja concluída pode resultar em uma verificação de volume ou uma leitura parcial do conteúdo do link.

Observe que não é seguro pressupor que isso apenas desaloque memória. Por exemplo, essa função também pode executar operações administrativas adicionais para a arquitetura do SIS. Portanto, chame essa função mesmo se sua operação de restauração for encerrada imediatamente depois.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                   |
| parâmetro<br/>                   | <dl> <dt>Sisbkup. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Sisbkup. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Sisbkup.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SisCreateRestoreStructure**](siscreaterestorestructure.md)
</dt> </dl>

 

