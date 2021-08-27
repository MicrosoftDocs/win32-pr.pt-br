---
title: Método GetRedirectableAddresses da classe Win32_TSSessionDirectory
description: Obtém a lista completa de endereços do DNS qualificados.
ms.assetid: 828079e7-472c-4428-97a0-2d5dedcdae91
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método GetRedirectableAddresses
- Método GetRedirectableAddresses Serviços de Área de Trabalho Remota, classe Win32_TSSessionDirectory
- Classe Win32_TSSessionDirectory Serviços de Área de Trabalho Remota, método GetRedirectableAddresses
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.GetRedirectableAddresses
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ff3e5dda8459361855c6ff2b287b71cbe02136b906e7defc816d4e7df727a08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120010089"
---
# <a name="getredirectableaddresses-method-of-the-win32_tssessiondirectory-class"></a>Método GetRedirectableAddresses da classe Win32 \_ TSSessionDirectory

Obtém a lista completa de endereços do DNS qualificados.

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetRedirectableAddresses(
  [in]  uint32 fTokenRedirection,
  [out] string IPAddresses[],
  [out] string AdapterNames[],
  [out] string NetConName[]
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*fTokenRedirection* \[ no\]
</dt> <dd>

Tipo: **UInt32**

Um sinalizador que indica se o redirecionamento de token deve ser usado.

</dd> <dt>

*IPAddresses* \[ fora\]
</dt> <dd>

Tipo: **cadeia \[ \] de caracteres**

A lista completa de endereços IP que estão disponíveis para redirecionamento.

</dd> <dt>

*Adaptadores* \[ fora\]
</dt> <dd>

Tipo: **cadeia \[ \] de caracteres**

A lista de nomes de adaptadores de rede que estão associados aos endereços que estão disponíveis para redirecionamento.

</dd> <dt>

*NetConName* \[ fora\]
</dt> <dd>

Tipo: **cadeia \[ \] de caracteres**

A lista de nomes de conexão de rede que estão associados aos endereços que estão disponíveis para redirecionamento.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **UInt32**

Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI. Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.

## <a name="remarks"></a>Comentários

os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\TerminalServices da CIMv2 raiz \\<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_TSSessionDirectory Win32**](win32-tssessiondirectory.md)
</dt> </dl>

 

