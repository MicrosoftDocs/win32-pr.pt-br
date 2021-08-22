---
title: Método GetPendingStartServerList da classe Win32_RDSHServer
description: Recupera uma lista de servidores aguardando para iniciar.
ms.assetid: 7af7a0e7-dc00-4e3a-8e0c-5987bd2bc3a2
ms.tgt_platform: multiple
keywords:
- Método GetPendingStartServerList Serviços de Área de Trabalho Remota
- Método GetPendingStartServerList Serviços de Área de Trabalho Remota , Win32_RDSHServer classe
- Win32_RDSHServer classe Serviços de Área de Trabalho Remota , método GetPendingStartServerList
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
ms.openlocfilehash: 61bb46512414c7057d7ec9db5ff4b6fab859f8bb9e6aec5c537250b0baa24e9a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119422646"
---
# <a name="getpendingstartserverlist-method-of-the-win32_rdshserver-class"></a>Método GetPendingStartServerList da classe \_ Win32 RDSHServer

Recupera uma lista de servidores aguardando para iniciar.

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetPendingStartServerList(
  [in]  uint32 maxServers,
  [out] string ServerFQDNs[]
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*maxServers* \[ Em\]
</dt> <dd>

O número máximo de servidores a retornar na lista.

</dd> <dt>

*ServerFQDNs* \[ out\]
</dt> <dd>

Em caso de sucesso, contém uma coleção de nomes de domínio totalmente qualificados dos servidores que estão aguardando o início.

</dd> </dl>

## <a name="remarks"></a>Comentários

A lista de servidores é redefinida após cada chamada, para que a próxima chamada não receba um servidor duplicado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                   |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                              |
| Namespace<br/>                | Raiz \\ cimv2 \\ rdms<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ RDSHServer**](win32-rdshserver.md)
</dt> </dl>

 

 





