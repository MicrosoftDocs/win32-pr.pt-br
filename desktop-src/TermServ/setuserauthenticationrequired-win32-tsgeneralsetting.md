---
title: Método SetUserAuthenticationRequired da classe Win32_TSGeneralSetting
description: Habilita ou desabilita o requisito de que os usuários devem ser autenticados no momento da conexão, definindo o valor da propriedade UserAuthenticationRequired.
ms.assetid: a0581326-fecc-4d23-87bf-3696c93366e8
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetUserAuthenticationRequired
- Método SetUserAuthenticationRequired Serviços de Área de Trabalho Remota, classe Win32_TSGeneralSetting
- Classe Win32_TSGeneralSetting Serviços de Área de Trabalho Remota, método SetUserAuthenticationRequired
topic_type:
- apiref
api_name:
- Win32_TSGeneralSetting.SetUserAuthenticationRequired
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b39c0eb711d2146130ff0fd879953fc71fcba965
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295874"
---
# <a name="setuserauthenticationrequired-method-of-the-win32_tsgeneralsetting-class"></a>Método SetUserAuthenticationRequired da classe Win32 \_ TSGeneralSetting

Habilita ou desabilita o requisito de que os usuários devem ser autenticados no momento da conexão, definindo o valor da propriedade **UserAuthenticationRequired** na classe [**Win32 \_ TSGeneralSetting**](win32-tsgeneralsetting.md) . Se **for true**, o que significa habilitado, o **UserAuthenticationRequired** exigirá a autenticação do usuário no momento da conexão para aumentar a proteção do servidor contra ataques à rede. Somente clientes protocolo RDP (RDP) que oferecem suporte a RDP versão 6,0 ou superior são capazes de se conectar. Para evitar interrupções para usuários remotos, é recomendável implantar clientes RDP que dão suporte à versão de protocolo apropriada antes de habilitar a propriedade.

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetUserAuthenticationRequired(
  [in] uint32 UserAuthenticationRequired
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*UserAuthenticationRequired* \[ no\]
</dt> <dd>

Indica se a autenticação do usuário é necessária.

<dt>

0 (0x0)
</dt> <dd>

Desabilitar o requisito de que o usuário deve ser autenticado

</dd> <dt>

1 (0x1)
</dt> <dd>

Habilita o requisito de que o usuário deve ser autenticado.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI. Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.

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
</dt> </dl>

 

