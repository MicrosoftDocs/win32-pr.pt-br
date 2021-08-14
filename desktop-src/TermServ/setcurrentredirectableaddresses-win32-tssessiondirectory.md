---
title: Método SetCurrentRedirectableAddresses da classe Win32_TSSessionDirectory
description: Define a lista configurada de endereços DNS qualificados que podem ser usados para redirecionamento.
ms.assetid: cad6a8a8-fdf1-406e-abeb-37acb396ac16
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetCurrentRedirectableAddresses
- Método SetCurrentRedirectableAddresses Serviços de Área de Trabalho Remota, classe Win32_TSSessionDirectory
- Classe Win32_TSSessionDirectory Serviços de Área de Trabalho Remota, método SetCurrentRedirectableAddresses
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetCurrentRedirectableAddresses
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cf1e9ab7b385111ccf91af9b4e3d6ed8bed0191f2d044c02a41705dbbc4f781
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117756096"
---
# <a name="setcurrentredirectableaddresses-method-of-the-win32_tssessiondirectory-class"></a>Método SetCurrentRedirectableAddresses da classe Win32 \_ TSSessionDirectory

O método **SetCurrentRedirectableAddresses** define a lista configurada de endereços DNS qualificados que podem ser usados para redirecionamento.

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetCurrentRedirectableAddresses(
  [in] uint32 fTokenRedirection,
  [in] string IPAddresses[]
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*fTokenRedirection* \[ no\]
</dt> <dd>

Tipo: **UInt32**

Um sinalizador que indica se o redirecionamento de token deve ser usado.

</dd> <dt>

*IPAddresses* \[ no\]
</dt> <dd>

Tipo: **cadeia \[ \] de caracteres**

Uma matriz de cadeias de caracteres que representa a lista de endereços IP qualificados do DNS que podem ser usados para redirecionamento.

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

 

