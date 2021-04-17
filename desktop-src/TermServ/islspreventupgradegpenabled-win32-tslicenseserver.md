---
title: Método IsLSPreventUpgradeGPEnabled da classe Win32_TSLicenseServer
description: Recupera se o \ 0034; impede a atualização da licença \ 0034; a configuração de política de grupo está habilitada no servidor de licença Área de Trabalho Remota.
ms.assetid: f78585b8-a50c-402b-ab20-f405eba0c079
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método IsLSPreventUpgradeGPEnabled
- Método IsLSPreventUpgradeGPEnabled Serviços de Área de Trabalho Remota, classe Win32_TSLicenseServer
- Classe Win32_TSLicenseServer Serviços de Área de Trabalho Remota, método IsLSPreventUpgradeGPEnabled
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsLSPreventUpgradeGPEnabled
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 205dc1ac05f5dca44297f8d80653ad51b7518d38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105754709"
---
# <a name="islspreventupgradegpenabled-method-of-the-win32_tslicenseserver-class"></a>Método IsLSPreventUpgradeGPEnabled da classe Win32 \_ TSLicenseServer

Recupera se a configuração da política de grupo "impedir atualização de licença" está habilitada no servidor de licença Área de Trabalho Remota.

## <a name="syntax"></a>Sintaxe


```mof
uint32 IsLSPreventUpgradeGPEnabled(
  [out] boolean Enabled
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Habilitado* \[ fora\]
</dt> <dd>

Valor booliano que indica se a configuração de política "impedir atualização de licença" está habilitada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o método tiver sucesso, ele retornará zero. Se o método não for bem-sucedido, ele retornará um valor diferente de zero. Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Comentários

Você deve ser um membro do grupo Administradores para chamar esse método.

Se a configuração de política "impedir atualização de licença" estiver habilitada, o servidor de licença emitirá apenas um RDS CAL temporário para o cliente se um RDS CAL apropriado para o servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) não estiver disponível.

A configuração de política está localizada no seguinte nó do editor de diretiva de grupo local:

Configuração do computador \\ modelos administrativos \\ componentes do Windows \\ \\ Licenciamento TS dos serviços de terminal

Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                            |
| Namespace<br/>                | Raiz\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_TSLicenseServer Win32**](win32-tslicenseserver.md)
</dt> </dl>

 

