---
title: Método SetColorDepth da classe Win32_TSClientSetting classe
description: O método SetColorDepth define a propriedade ColorDepth para a classe .
ms.assetid: 1ab8ac41-cbbf-4077-b91e-692856ccba42
ms.tgt_platform: multiple
keywords:
- Método SetColorDepth Serviços de Área de Trabalho Remota
- Método SetColorDepth Serviços de Área de Trabalho Remota , Win32_TSClientSetting classe
- Win32_TSClientSetting classe Serviços de Área de Trabalho Remota , método SetColorDepth
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
ms.openlocfilehash: da2c7f31ef04fdfb9dcbfee5e1ca3dcec1386a7dbd0c20824b00bdfe41ac6d48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999856"
---
# <a name="setcolordepth-method-of-the-win32_tsclientsetting-class"></a>Método SetColorDepth da classe \_ Win32 TSClientSetting

O **método SetColorDepth** define a **propriedade ColorDepth** para a classe .

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetColorDepth(
  [in] uint32 ColorDepth
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ColorDepth* \[ Em\]
</dt> <dd>

O novo valor para a **propriedade ColorDepth.**

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

<span id="3"></span>**3**


</dt> <dd>

16 bits por pixel

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**4**


</dt> <dd>

24 bits por pixel

</dd> <dt>

<span id="5"></span>

<span id="5"></span>**5**


</dt> <dd>

32 bits por pixel

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna Êxito em caso de êxito; caso contrário, retorna um código de erro WMI. Consulte Serviços de Área de Trabalho Remota códigos de erro do provedor [WMI](terminal-services-wmi-provider-error-codes.md) para ver uma lista desses valores. O método retornará um erro se a configuração estiver sob controle de política de grupo.

## <a name="remarks"></a>Comentários

arquivos Managed Object Format (MOF) contêm as definições para classes WMI (Instrumentação de Gerenciamento de Windows). Os arquivos MOF não são instalados como parte do Microsoft Windows Software Development Kit (SDK). Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, [consulte Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\CiMv2 \\ TerminalServices raiz<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ TSClientSetting**](win32-tsclientsetting.md)
</dt> </dl>

 

