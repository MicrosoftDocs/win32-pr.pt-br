---
title: Método SetSessionDirectoryExposeServerIP da classe Win32_TSSessionDirectory
description: Define a propriedade SessionDirectoryExposeServerIP.
ms.assetid: ae9a0c72-0a0a-42a0-a233-13da1efe60ef
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetSessionDirectoryExposeServerIP
- Método SetSessionDirectoryExposeServerIP Serviços de Área de Trabalho Remota, classe Win32_TSSessionDirectory
- Classe Win32_TSSessionDirectory Serviços de Área de Trabalho Remota, método SetSessionDirectoryExposeServerIP
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetSessionDirectoryExposeServerIP
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc03f175e780d63eed3881b9146116702a30a02a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918303"
---
# <a name="setsessiondirectoryexposeserverip-method-of-the-win32_tssessiondirectory-class"></a>Método SetSessionDirectoryExposeServerIP da classe Win32 \_ TSSessionDirectory

Define a propriedade **SessionDirectoryExposeServerIP** .

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetSessionDirectoryExposeServerIP(
  [in] uint32 SessionDirectoryExposeServerIP
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*SessionDirectoryExposeServerIP* \[ no\]
</dt> <dd>

Tipo: **UInt32**

Sinalizador desabilitando ou habilitando a propriedade **SessionDirectoryExposeServerIP** que permite ou nega a recuperação do endereço IP para o diretório de sessão.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Desabilite a propriedade.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Habilite a propriedade.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **UInt32**

Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI. Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores. O método retornará um erro se a configuração estiver sob controle de diretiva de grupo.

## <a name="remarks"></a>Comentários

Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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

 

