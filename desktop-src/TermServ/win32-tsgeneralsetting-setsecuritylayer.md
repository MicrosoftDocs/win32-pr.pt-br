---
title: Método SetSecurityLayer da classe Win32_TSGeneralSetting
description: O método SetSecurityLayer define a camada de segurança.
ms.assetid: 3b894494-2180-4f1d-8e67-a66c679d286c
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetSecurityLayer
- Método SetSecurityLayer Serviços de Área de Trabalho Remota, classe Win32_TSGeneralSetting
- Classe Win32_TSGeneralSetting Serviços de Área de Trabalho Remota, método SetSecurityLayer
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
ms.openlocfilehash: b5e04c3f7e5a58ec8de345d570e36b35c7eb1e7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918548"
---
# <a name="setsecuritylayer-method-of-the-win32_tsgeneralsetting-class"></a>Método SetSecurityLayer da classe Win32 \_ TSGeneralSetting

O método **SetSecurityLayer** define a camada de segurança.

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetSecurityLayer(
  [in] uint32 SecurityLayer
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*SecurityLayer* \[ no\]
</dt> <dd>

A camada de segurança a ser definida. Se o nível de criptografia atual for 1, um valor de 2 para *SecurityLayer* não será válido.

<dt>

<span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>

<span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>**Camada de segurança RDP** (0)


</dt> <dd>

A comunicação entre o servidor e o cliente usará a criptografia RDP nativa.

</dd> <dt>

<span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>

<span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>**Negociar** (1)


</dt> <dd>

A camada mais segura com suporte do cliente será usada. Se houver suporte, o SSL (TLS 1,0) será usado.

</dd> <dt>

<span id="SSL"></span><span id="ssl"></span>

<span id="SSL"></span><span id="ssl"></span>**SSL** (2)


</dt> <dd>

O SSL (TLS 1,0) será usado para autenticação de servidor, bem como para criptografar todos os dados transferidos entre o servidor e o cliente. Essa configuração requer que o servidor tenha um certificado compatível com SSL. Essa configuração não é compatível com um valor de **MinEncryptionLevel** de 1.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna êxito em caso de êxito, caso contrário retorna um código de erro WMI. Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.

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

[**\_TSGeneralSetting Win32**](win32-tsgeneralsetting.md)
</dt> <dt>

[**SetEncryptionLevel**](win32-tsgeneralsetting-setencryptionlevel.md)
</dt> </dl>

 

