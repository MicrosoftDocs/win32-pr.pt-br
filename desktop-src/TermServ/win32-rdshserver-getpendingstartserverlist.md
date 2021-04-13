---
title: Método GetPendingStartServerList da classe Win32_RDSHServer
description: Recupera uma lista de servidores que estão aguardando para serem iniciados.
ms.assetid: 7af7a0e7-dc00-4e3a-8e0c-5987bd2bc3a2
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método GetPendingStartServerList
- Método GetPendingStartServerList Serviços de Área de Trabalho Remota, classe Win32_RDSHServer
- Classe Win32_RDSHServer Serviços de Área de Trabalho Remota, método GetPendingStartServerList
topic_type:
- apiref
api_name:
- Win32_RDSHServer.GetPendingStartServerList
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99b96453b33f931b18d89f13413513d3baf82bfb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369665"
---
# <a name="getpendingstartserverlist-method-of-the-win32_rdshserver-class"></a>Método GetPendingStartServerList da classe Win32 \_ RDSHServer

Recupera uma lista de servidores que estão aguardando para serem iniciados.

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetPendingStartServerList(
  [in]  uint32 maxServers,
  [out] string ServerFQDNs[]
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*maxServers* \[ no\]
</dt> <dd>

O número máximo de servidores a serem retornados na lista.

</dd> <dt>

*ServerFQDNs* \[ fora\]
</dt> <dd>

Em caso de sucesso, contém uma coleção de nomes de domínio totalmente qualificados dos servidores que estão aguardando para iniciar.

</dd> </dl>

## <a name="remarks"></a>Comentários

A lista de servidores é redefinida após cada chamada, para que a próxima chamada não obtenha um servidor duplicado.

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

 

 





