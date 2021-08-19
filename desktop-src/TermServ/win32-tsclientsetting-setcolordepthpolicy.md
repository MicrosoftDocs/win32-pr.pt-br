---
title: Método SetColorDepthPolicy da classe Win32_TSClientSetting
description: O método SetColorDepthPolicy define a propriedade ColorDepthPolicy para a classe .
ms.assetid: 7a8c2b51-5f7a-4188-aae0-0b2d47d043bd
ms.tgt_platform: multiple
keywords:
- Método SetColorDepthPolicy Serviços de Área de Trabalho Remota
- Método SetColorDepthPolicy Serviços de Área de Trabalho Remota , Win32_TSClientSetting classe
- Win32_TSClientSetting classe Serviços de Área de Trabalho Remota , método SetColorDepthPolicy
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetColorDepthPolicy
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78ecb53500a65c997ace21865492a0a473c2799bd38a3876c4676aaea4120610
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999836"
---
# <a name="setcolordepthpolicy-method-of-the-win32_tsclientsetting-class"></a>Método SetColorDepthPolicy da classe \_ Win32 TSClientSetting

O **método SetColorDepthPolicy** define a **propriedade ColorDepthPolicy** para a classe .

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetColorDepthPolicy(
  [in] uint32 ColorDepthPolicy
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ColorDepthPolicy* \[ Em\]
</dt> <dd>

Sinalizar desabilitando ou habilitando a **propriedade SetColorDepthPolicy,** que especifica se deve substituir a configuração de cor máxima do usuário.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Habilita a propriedade .

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Desabilite a propriedade .

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

 

