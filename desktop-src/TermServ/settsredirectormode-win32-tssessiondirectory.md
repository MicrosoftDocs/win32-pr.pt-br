---
title: Método SetTSRedirectorMode da classe Win32_TSSessionDirectory
description: Define o valor para indicar se o servidor atuará como um redirecionador Serviços de Área de Trabalho Remota.
ms.assetid: abdb92df-1e49-4445-ba02-bb83fd1ca541
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetTSRedirectorMode
- Método SetTSRedirectorMode Serviços de Área de Trabalho Remota, classe Win32_TSSessionDirectory
- Classe Win32_TSSessionDirectory Serviços de Área de Trabalho Remota, método SetTSRedirectorMode
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetTSRedirectorMode
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6350d4b9a4858991616d45eb2b1092fe406c59b55b11c494a7f19be53dbb60ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118127272"
---
# <a name="settsredirectormode-method-of-the-win32_tssessiondirectory-class"></a>Método SetTSRedirectorMode da classe Win32 \_ TSSessionDirectory

Define o valor para indicar se o servidor atuará como um redirecionador Serviços de Área de Trabalho Remota.

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetTSRedirectorMode(
  [in] uint32 TSRedirValue
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*TSRedirValue* \[ no\]
</dt> <dd>

Tipo: **UInt32**

Especifica se o servidor atuará como um redirecionador Serviços de Área de Trabalho Remota. Isso pode ser um dos valores a seguir.

<dt>

0
</dt> <dd>

O servidor atuará como um redirecionador Serviços de Área de Trabalho Remota.

</dd> <dt>

1
</dt> <dd>

O servidor não funcionará como um redirecionador de Serviços de Área de Trabalho Remota.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **UInt32**

Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI. Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores. O método retornará um erro se a configuração estiver sob controle de diretiva de grupo.

## <a name="remarks"></a>Comentários

os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2<br/>                                                       |
| Fim do suporte do cliente<br/>    | Nenhum compatível<br/>                                                               |
| Fim do suporte do servidor<br/>    | Windows Server 2008 R2<br/>                                                       |
| Namespace<br/>                | \\TerminalServices da CIMv2 raiz \\<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_TSSessionDirectory Win32**](win32-tssessiondirectory.md)
</dt> </dl>

 

