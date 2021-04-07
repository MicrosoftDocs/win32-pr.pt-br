---
title: Método SetVirtualIPActive da classe Win32_TSVirtualIP
description: Define o valor da propriedade VirtualIPActive.
ms.assetid: e485aeb1-afdf-4572-bac7-daa80d903edc
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetVirtualIPActive
- Método SetVirtualIPActive Serviços de Área de Trabalho Remota, classe Win32_TSVirtualIP
- Classe Win32_TSVirtualIP Serviços de Área de Trabalho Remota, método SetVirtualIPActive
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
ms.openlocfilehash: 06534c967c5d86a7a19c060254b3b988ff98b17e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918645"
---
# <a name="setvirtualipactive-method-of-the-win32_tsvirtualip-class"></a>Método SetVirtualIPActive da classe Win32 \_ TSVirtualIP

Define o valor da propriedade **VirtualIPActive** .

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetVirtualIPActive(
  [in] uint32 VirtualIPActive
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*VirtualIPActive* \[ no\]
</dt> <dd>

Tipo: **UInt32**

Especifica se a virtualização de IP está ativa no servidor. Isso pode ser um dos valores a seguir.

<dt>

zero
</dt> <dd>

A virtualização de IP não está ativa.

</dd> <dt>

diferente
</dt> <dd>

A virtualização de IP está ativa.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **UInt32**

Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI. Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores. O método retornará um erro se a configuração estiver sob controle de diretiva de grupo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2<br/>                                                       |
| Namespace<br/>                | \\TerminalServices da CIMv2 raiz \\<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_TSVirtualIP Win32**](win32-tsvirtualip.md)
</dt> </dl>

 

 





