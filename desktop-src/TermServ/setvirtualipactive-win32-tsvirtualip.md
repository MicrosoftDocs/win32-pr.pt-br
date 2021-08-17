---
title: Método SetVirtualIPActive da classe Win32_TSVirtualIP
description: Define o valor da propriedade VirtualIPActive.
ms.assetid: e485aeb1-afdf-4572-bac7-daa80d903edc
ms.tgt_platform: multiple
keywords:
- Método SetVirtualIPActive Serviços de Área de Trabalho Remota
- Método SetVirtualIPActive Serviços de Área de Trabalho Remota , Win32_TSVirtualIP classe
- Win32_TSVirtualIP classe Serviços de Área de Trabalho Remota , método SetVirtualIPActive
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.SetVirtualIPActive
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ab43a007a2a8b04e91d5225e648d5667a87c468cbd52c005d85f4ba6496c919
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118850915"
---
# <a name="setvirtualipactive-method-of-the-win32_tsvirtualip-class"></a>Método SetVirtualIPActive da classe \_ TSVirtualIP do Win32

Define o **valor da propriedade VirtualIPActive.**

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetVirtualIPActive(
  [in] uint32 VirtualIPActive
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*VirtualIPActive* \[ Em\]
</dt> <dd>

Tipo: **uint32**

Especifica se a virtualização de IP está ativa no servidor. Esse pode ser um dos valores a seguir.

<dt>

zero
</dt> <dd>

A virtualização de IP não está ativa.

</dd> <dt>

Zero
</dt> <dd>

A virtualização de IP está ativa.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **uint32**

Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI. Consulte Serviços de Área de Trabalho Remota códigos de erro do provedor [WMI](terminal-services-wmi-provider-error-codes.md) para ver uma lista desses valores. O método retornará um erro se a configuração estiver sob controle de política de grupo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2<br/>                                                       |
| Namespace<br/>                | \\CiMv2 \\ TerminalServices raiz<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ TSVirtualIP**](win32-tsvirtualip.md)
</dt> </dl>

 

 





