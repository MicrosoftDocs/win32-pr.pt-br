---
title: Método TestAndSetState da classe Win32_RDSHServer
description: Compara o estado atual com o termo especificado; Se as duas corresponderem, o estado será definido como um novo valor. Independentemente da correspondência, o estado atual também é retornado.
ms.assetid: f1bb0076-251b-4c0d-92f9-1c460e1b26bb
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método TestAndSetState
- Método TestAndSetState Serviços de Área de Trabalho Remota, classe Win32_RDSHServer
- Classe Win32_RDSHServer Serviços de Área de Trabalho Remota, método TestAndSetState
topic_type:
- apiref
api_name:
- Win32_RDSHServer.TestAndSetState
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ff4c9b616c2a288f5f39b240d71b2611e25d45f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085657"
---
# <a name="testandsetstate-method-of-the-win32_rdshserver-class"></a>Método TestAndSetState da classe Win32 \_ RDSHServer

Compara o estado atual com o termo especificado; Se as duas corresponderem, o estado será definido como um novo valor. Independentemente da correspondência, o estado atual também é retornado.

## <a name="syntax"></a>Sintaxe


```mof
uint32 TestAndSetState(
  [in]  uint32 Comparand,
  [in]  uint32 NewState,
  [out] uint32 InitState
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Termo* \[ no\]
</dt> <dd>

Um valor a ser comparado com o estado atual; Se os dois valores corresponderem, o estado será definido como *NewState*.

</dd> <dt>

*NewState* \[ no\]
</dt> <dd>

O novo valor do estado.

</dd> <dt>

*Initstate* \[ fora\]
</dt> <dd>

Em caso de êxito ou falha, retorna o estado atual.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                   |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                              |
| Namespace<br/>                | \\RDMs cimv2 \\ raiz<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_RDSHServer Win32**](win32-rdshserver.md)
</dt> </dl>

 

 





