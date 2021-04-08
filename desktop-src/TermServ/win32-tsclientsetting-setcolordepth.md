---
title: Método SetColorDepth da classe Win32_TSClientSetting
description: O método SetColorDepth define a propriedade ColorDepth para a classe.
ms.assetid: 1ab8ac41-cbbf-4077-b91e-692856ccba42
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetColorDepth
- Método SetColorDepth Serviços de Área de Trabalho Remota, classe Win32_TSClientSetting
- Classe Win32_TSClientSetting Serviços de Área de Trabalho Remota, método SetColorDepth
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetColorDepth
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97f2b05c6b8ff02b78f48ff45751bdc8e57ef46a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919036"
---
# <a name="setcolordepth-method-of-the-win32_tsclientsetting-class"></a>Método SetColorDepth da classe Win32 \_ TSClientSetting

O método **SetColorDepth** define a propriedade **ColorDepth** para a classe.

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetColorDepth(
  [in] uint32 ColorDepth
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ColorDepth* \[ no\]
</dt> <dd>

O novo valor para a propriedade **ColorDepth** .

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

8 bits por pixel

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

15 bits por pixel

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**Beta**


</dt> <dd>

16 bits por pixel

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**quatro**


</dt> <dd>

24 bits por pixel

</dd> <dt>

<span id="5"></span>

<span id="5"></span>**05**


</dt> <dd>

32 bits por pixel

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna êxito em caso de êxito, caso contrário retorna um código de erro WMI. Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores. O método retornará um erro se a configuração estiver sob controle de diretiva de grupo.

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



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_TSClientSetting Win32**](win32-tsclientsetting.md)
</dt> </dl>

 

