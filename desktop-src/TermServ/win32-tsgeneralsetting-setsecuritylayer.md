---
title: Método SetSecurityLayer da Win32_TSGeneralSetting classe
description: O método SetSecurityLayer define a camada de segurança.
ms.assetid: 3b894494-2180-4f1d-8e67-a66c679d286c
ms.tgt_platform: multiple
keywords:
- Método SetSecurityLayer Serviços de Área de Trabalho Remota
- Método SetSecurityLayer Serviços de Área de Trabalho Remota , Win32_TSGeneralSetting classe
- Win32_TSGeneralSetting classe Serviços de Área de Trabalho Remota , método SetSecurityLayer
topic_type:
- apiref
api_name:
- Win32_TSGeneralSetting.SetSecurityLayer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e01f761b63be028e2c507644f160b6742f9d781e517ea03ce549e3ac84419c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513866"
---
# <a name="setsecuritylayer-method-of-the-win32_tsgeneralsetting-class"></a>Método SetSecurityLayer da classe Win32 \_ TSGeneralSetting

O **método SetSecurityLayer** define a camada de segurança.

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetSecurityLayer(
  [in] uint32 SecurityLayer
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*SecurityLayer* \[ Em\]
</dt> <dd>

A camada de segurança a ser definida. Se o Nível de Criptografia atual for 1, um valor de 2 para *SecurityLayer* não será válido.

<dt>

<span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>

<span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>**Camada de segurança RDP** (0)


</dt> <dd>

A comunicação entre o servidor e o cliente usará a criptografia RDP nativa.

</dd> <dt>

<span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>

<span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>**Negociar** (1)


</dt> <dd>

A camada mais segura com suporte pelo cliente será usada. Se tiver suporte, o SSL (TLS 1.0) será usado.

</dd> <dt>

<span id="SSL"></span><span id="ssl"></span>

<span id="SSL"></span><span id="ssl"></span>**SSL** (2)


</dt> <dd>

O SSL (TLS 1.0) será usado para autenticação de servidor, bem como para criptografar todos os dados transferidos entre o servidor e o cliente. Essa configuração exige que o servidor tenha um certificado compatível com SSL. Essa configuração não é compatível com um **valor MinEncryptionLevel** de 1.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna Êxito em caso de êxito; caso contrário, retorna um código de erro WMI. Consulte Serviços de Área de Trabalho Remota códigos de erro do provedor [WMI](terminal-services-wmi-provider-error-codes.md) para ver uma lista desses valores.

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

[**Win32 \_ TSGeneralSetting**](win32-tsgeneralsetting.md)
</dt> <dt>

[**SetEncryptionLevel**](win32-tsgeneralsetting-setencryptionlevel.md)
</dt> </dl>

 

