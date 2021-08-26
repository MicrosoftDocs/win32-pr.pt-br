---
title: Método DeleteEx da classe Win32_SessionBrokerFarmAccount classe
description: A classe SessionBrokerFarmAccount do Win32 não está mais disponível para uso desde \_ Windows Server 2012. | Método DeleteEx da classe Win32_SessionBrokerFarmAccount classe
ms.assetid: d30c5d3e-f63c-4b21-85ae-a0b8d5868d64
ms.tgt_platform: multiple
keywords:
- Método DeleteEx Serviços de Área de Trabalho Remota
- Classe Serviços de Área de Trabalho Remota , Win32_SessionBrokerFarmAccount DeleteEx
- Win32_SessionBrokerFarmAccount classe Serviços de Área de Trabalho Remota , método DeleteEx
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
ms.openlocfilehash: aa891c874c9592ed11b2aa0840913e67daa7226a93f6f746cf74c45a0454a476
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080216"
---
# <a name="deleteex-method-of-the-win32_sessionbrokerfarmaccount-class"></a>Método DeleteEx da classe \_ SessionBrokerFarmAccount do Win32

\[A [**classe \_ SessionBrokerFarmAccount do Win32**](win32-sessionbrokerfarmaccount.md) não está mais disponível para uso desde Windows Server 2012.\]

Exclui a conta do farm.

## <a name="syntax"></a>Sintaxe


```mof
uint32 DeleteEx(
  [in] boolean DeleteComputerObject
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*DeleteComputerObject* \[ Em\]
</dt> <dd>

Indica se o objeto de computador associado ao farm deve ser removido do Active Directory.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI. Consulte Serviços de Área de Trabalho Remota códigos de erro do provedor [WMI](terminal-services-wmi-provider-error-codes.md) para ver uma lista desses valores.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2<br/>                                                      |
| Fim do suporte ao cliente<br/>    | Nenhum compatível<br/>                                                              |
| Fim do suporte ao servidor<br/>    | Windows Server 2008 R2<br/>                                                      |
| Namespace<br/>                | \\CiMv2 \\ TerminalServices raiz<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ SessionBrokerFarmAccount**](win32-sessionbrokerfarmaccount.md)
</dt> </dl>

 

 





