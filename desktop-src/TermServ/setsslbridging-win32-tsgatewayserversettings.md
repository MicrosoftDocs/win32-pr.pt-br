---
title: Método SetSslBridging da classe Win32_TSGatewayServerSettings
description: Define o tipo de ponte SSL a ser usado pelo servidor de gateway de Área de Trabalho Remota (gateway de área de trabalho remota).
ms.assetid: 11885b8b-491e-4d90-b4d4-f0a0fbe68cb1
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetSslBridging
- Método SetSslBridging Serviços de Área de Trabalho Remota, classe Win32_TSGatewayServerSettings
- Classe Win32_TSGatewayServerSettings Serviços de Área de Trabalho Remota, método SetSslBridging
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetSslBridging
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77181fb8d8661ec7ea7dc0ce70532281fb9c1bde
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369720"
---
# <a name="setsslbridging-method-of-the-win32_tsgatewayserversettings-class"></a>Método SetSslBridging da classe Win32 \_ TSGatewayServerSettings

Define o tipo de ponte SSL a ser usado pelo servidor de gateway de Área de Trabalho Remota (gateway de área de trabalho remota). Esse valor é armazenado na propriedade **SslBridging** .

> [!IMPORTANT]
> Quando o tipo de ponte SSL é alterado com esse método, o serviço de gateway de área de trabalho remota deve ser reiniciado para fazer com que essa alteração entre em vigor.

 

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetSslBridging(
  [in] uint32 SslBridging
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*SslBridging* \[ no\]
</dt> <dd>

Tipo: **UInt32**

Especifica o novo valor de ponte SSL. Isso pode ser um dos valores a seguir.

<dt>

0
</dt> <dd>

Sem ponte SSL.

</dd> <dt>

1
</dt> <dd>

Conexão HTTPS com HTTP.

</dd> <dt>

2
</dt> <dd>

Conexão HTTPS com HTTPS.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **UInt32**

Se o método tiver sucesso, ele retornará zero. Se o método não for bem-sucedido, ele retornará um valor diferente de zero. Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Comentários

Você deve ser um membro do grupo Administradores para chamar esse método.

Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2<br/>                                                        |
| Namespace<br/>                | \\TerminalServices da CIMv2 raiz \\<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TS. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_TSGatewayServerSettings Win32**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

