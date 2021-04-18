---
title: Método DeleteEx da classe Win32_SessionBrokerFarmAccount
description: A \_ classe Win32 SessionBrokerFarmAccount não está mais disponível para uso a partir do Windows Server 2012. | Método DeleteEx da classe Win32_SessionBrokerFarmAccount
ms.assetid: d30c5d3e-f63c-4b21-85ae-a0b8d5868d64
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método DeleteEx
- Método DeleteEx Serviços de Área de Trabalho Remota, classe Win32_SessionBrokerFarmAccount
- Classe Win32_SessionBrokerFarmAccount Serviços de Área de Trabalho Remota, método DeleteEx
topic_type:
- apiref
api_name:
- Win32_SessionBrokerFarmAccount.DeleteEx
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdad7b1c7af85337ace59690bb44f4309254eb76
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105810445"
---
# <a name="deleteex-method-of-the-win32_sessionbrokerfarmaccount-class"></a>Método DeleteEx da classe Win32 \_ SessionBrokerFarmAccount

\[A classe [**Win32 \_ SessionBrokerFarmAccount**](win32-sessionbrokerfarmaccount.md) não está mais disponível para uso a partir do Windows Server 2012.\]

Exclui a conta do farm.

## <a name="syntax"></a>Sintaxe


```mof
uint32 DeleteEx(
  [in] boolean DeleteComputerObject
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*DeleteComputerObject* \[ no\]
</dt> <dd>

Indica se o objeto de computador associado ao farm deve ser removido da Active Directory.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI. Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2<br/>                                                      |
| Fim do suporte do cliente<br/>    | Nenhum compatível<br/>                                                              |
| Fim do suporte do servidor<br/>    | Windows Server 2008 R2<br/>                                                      |
| Namespace<br/>                | \\TerminalServices da CIMv2 raiz \\<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_SessionBrokerFarmAccount Win32**](win32-sessionbrokerfarmaccount.md)
</dt> </dl>

 

 





