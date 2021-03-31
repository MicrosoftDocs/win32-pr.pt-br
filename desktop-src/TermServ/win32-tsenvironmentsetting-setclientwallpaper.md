---
title: Método SetClientWallPaper da classe Win32_TSEnvironmentSetting
description: O método SetClientWallPaper define a propriedade ClientWallPaper.
ms.assetid: 08c41df4-5a3c-4799-bb64-61f414814d0c
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetClientWallPaper
- Método SetClientWallPaper Serviços de Área de Trabalho Remota, classe Win32_TSEnvironmentSetting
- Classe Win32_TSEnvironmentSetting Serviços de Área de Trabalho Remota, método SetClientWallPaper
topic_type:
- apiref
api_name:
- Win32_TSEnvironmentSetting.SetClientWallPaper
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04ae476134cf526602a059b4714cded6fd6c990e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644589"
---
# <a name="setclientwallpaper-method-of-the-win32_tsenvironmentsetting-class"></a>Método SetClientWallPaper da classe Win32 \_ TSEnvironmentSetting

O método **SetClientWallPaper** define a propriedade **ClientWallPaper** .

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetClientWallPaper(
  [in] uint32 ClientWallPaper
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ClientWallPaper* \[ no\]
</dt> <dd>

Sinalizador desabilitando ou habilitando a propriedade **ClientWallPaper** , que especifica se a imagem de plano de fundo (ou papel de parede) é exibida no cliente.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

A imagem em segundo plano (ou papel de parede) não é exibida no cliente.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

A imagem em segundo plano (ou papel de parede) é exibida no cliente.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI. Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores. O método retornará um erro se a configuração estiver sob controle de diretiva de grupo.

## <a name="remarks"></a>Comentários

Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\TerminalServices da CIMv2 raiz \\<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**\_TSEnvironmentSetting Win32**](win32-tsenvironmentsetting.md)
</dt> </dl>

 

