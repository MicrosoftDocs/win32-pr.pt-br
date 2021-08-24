---
title: Método SetSessionDirectoryActive da classe Win32_TSSessionDirectory
description: O método SetSessionDirectoryActive define a propriedade SessionDirectoryActive.
ms.assetid: b2175d1a-b62f-4bdf-9122-76e85233fba4
ms.tgt_platform: multiple
keywords:
- Método SetSessionDirectoryActive Serviços de Área de Trabalho Remota
- Método SetSessionDirectoryActive Serviços de Área de Trabalho Remota , Win32_TSSessionDirectory classe
- Win32_TSSessionDirectory classe Serviços de Área de Trabalho Remota , método SetSessionDirectoryActive
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetSessionDirectoryActive
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ae44c471c653a3fcdfbab33ab70178b53c95715cce7cfba63defa9c96c1ab23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769346"
---
# <a name="setsessiondirectoryactive-method-of-the-win32_tssessiondirectory-class"></a>Método SetSessionDirectoryActive da classe \_ Win32 TSSessionDirectory

O **método SetSessionDirectoryActive** define a **propriedade SessionDirectoryActive.**

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetSessionDirectoryActive(
  [in] uint32 SessionDirectoryActive
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*SessionDirectoryActive* \[ Em\]
</dt> <dd>

Tipo: **uint32**

Sinalizar a desabilitação ou a habilitação do serviço diretório de sessão.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Desabilite o serviço diretório de sessão.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Habilita o serviço diretório de sessão.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **uint32**

Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI. Consulte Serviços de Área de Trabalho Remota códigos de erro do provedor [WMI](terminal-services-wmi-provider-error-codes.md) para ver uma lista desses valores. O método retornará um erro se a configuração estiver sob controle de política de grupo.

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

 

