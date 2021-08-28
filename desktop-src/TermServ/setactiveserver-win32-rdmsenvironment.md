---
title: Método SetActiveServer da classe Win32_RDMSEnvironment
description: Define o FQDN do ambiente de serviços de gerenciamento de Área de Trabalho Remota (RDMS) para o nó atual.
ms.assetid: ed7b71cf-c3a4-4d2f-856a-31332f94fac9
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetActiveServer
- Método SetActiveServer Serviços de Área de Trabalho Remota, classe Win32_RDMSEnvironment
- Classe Win32_RDMSEnvironment Serviços de Área de Trabalho Remota, método SetActiveServer
topic_type:
- apiref
api_name:
- Win32_RDMSEnvironment.SetActiveServer
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b68a8f9c6661e78932893ef25278234fb4c944d22297cb87cc95aebe9bc8d8ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865486"
---
# <a name="setactiveserver-method-of-the-win32_rdmsenvironment-class"></a>Método SetActiveServer da classe Win32 \_ RDMSEnvironment

Define o FQDN do ambiente de serviços de gerenciamento de Área de Trabalho Remota (RDMS) para o nó atual.

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetActiveServer();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                   |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                              |
| Namespace<br/>                | \\RDMs CIMv2 \\ raiz<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_RDMSEnvironment Win32**](win32-rdmsenvironment.md)
</dt> </dl>

 

 





