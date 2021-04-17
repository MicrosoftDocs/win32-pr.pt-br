---
title: Método SetVirtualIPMode da classe Win32_TSVirtualIP
description: Define o valor da propriedade VirtualIPMode.
ms.assetid: d4b39566-ad2a-493b-8022-c006a857043d
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetVirtualIPMode
- Método SetVirtualIPMode Serviços de Área de Trabalho Remota, classe Win32_TSVirtualIP
- Classe Win32_TSVirtualIP Serviços de Área de Trabalho Remota, método SetVirtualIPMode
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.SetVirtualIPMode
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 250633f5d41f5a4a7cb06a17ba9ae45bb444a018
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105780097"
---
# <a name="setvirtualipmode-method-of-the-win32_tsvirtualip-class"></a>Método SetVirtualIPMode da classe Win32 \_ TSVirtualIP

Define o valor da propriedade **VirtualIPMode** .

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetVirtualIPMode(
  [in] uint32 VirtualIPMode
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*VirtualIPMode* \[ no\]
</dt> <dd>

Tipo: **UInt32**

Especifica qual modo de virtualização de IP está sendo usado no servidor. Isso pode ser um dos valores a seguir.

<dt>

0
</dt> <dd>

O modo de virtualização de IP é por sessão.

</dd> <dt>

1
</dt> <dd>

O modo de virtualização de IP é por usuário.

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

 

 





