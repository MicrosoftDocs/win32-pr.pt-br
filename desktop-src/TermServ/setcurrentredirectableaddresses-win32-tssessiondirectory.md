---
title: Método SetCurrentRedirectableAddresses da classe Win32_TSSessionDirectory
description: Define a lista configurada de endereços qualificados para DNS que podem ser usados para redirecionamento.
ms.assetid: cad6a8a8-fdf1-406e-abeb-37acb396ac16
ms.tgt_platform: multiple
keywords:
- Método SetCurrentRedirectableAddresses Serviços de Área de Trabalho Remota
- Método SetCurrentRedirectableAddresses Serviços de Área de Trabalho Remota , Win32_TSSessionDirectory classe
- Win32_TSSessionDirectory classe Serviços de Área de Trabalho Remota , método SetCurrentRedirectableAddresses
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
# <a name="setcurrentredirectableaddresses-method-of-the-win32_tssessiondirectory-class"></a>Método SetCurrentRedirectableAddresses da classe \_ Win32 TSSessionDirectory

O **método SetCurrentRedirectableAddresses** define a lista configurada de endereços qualificados para DNS que podem ser usados para redirecionamento.

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetCurrentRedirectableAddresses(
  [in] uint32 fTokenRedirection,
  [in] string IPAddresses[]
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*fTokenRedirection* \[ Em\]
</dt> <dd>

Tipo: **uint32**

Um sinalizador que indica se o redirecionamento de token deve ser usado.

</dd> <dt>

*IPAddresses* \[ Em\]
</dt> <dd>

Tipo: cadeia **de caracteres \[ \]**

Uma matriz de cadeias de caracteres que representa a lista de endereços IP qualificados para DNS que podem ser usados para redirecionamento.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **uint32**

Retorna 0 em caso de êxito; caso contrário, retornará um código de erro WMI. Consulte Serviços de Área de Trabalho Remota códigos de erro do provedor [WMI](terminal-services-wmi-provider-error-codes.md) para ver uma lista desses valores.

## <a name="remarks"></a>Comentários

arquivos Managed Object Format (MOF) contêm as definições para classes WMI (Instrumentação de Gerenciamento de Windows). Os arquivos MOF não são instalados como parte do Microsoft Windows Software Development Kit (SDK). Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, [consulte Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\CiMv2 \\ TerminalServices raiz<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ TSSessionDirectory**](win32-tssessiondirectory.md)
</dt> </dl>

 

