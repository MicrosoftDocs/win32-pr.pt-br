---
title: Método IsLSPreventUpgradeGPEnabled da classe Win32_TSLicenseServer
description: Recupera se o \ 0034;impedir a atualização de licença \ 0034; A configuração de política de grupo está habilitada no Área de Trabalho Remota de licença.
ms.assetid: f78585b8-a50c-402b-ab20-f405eba0c079
ms.tgt_platform: multiple
keywords:
- Método IsLSPreventUpgradeGPEnabled Serviços de Área de Trabalho Remota
- Método IsLSPreventUpgradeGPEnabled Serviços de Área de Trabalho Remota classe Win32_TSLicenseServer ,
- Win32_TSLicenseServer classe Serviços de Área de Trabalho Remota , método IsLSPreventUpgradeGPEnabled
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
ms.openlocfilehash: 7958df7d153db0abafd8e463f22a181f2e5a639afa5c21cb7529a9cd5c005c5b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119511686"
---
# <a name="islspreventupgradegpenabled-method-of-the-win32_tslicenseserver-class"></a>Método IsLSPreventUpgradeGPEnabled da classe \_ Win32 TSLicenseServer

Recupera se a configuração de política de grupo "impedir a atualização de licença" está habilitada no servidor Área de Trabalho Remota licença.

## <a name="syntax"></a>Sintaxe


```mof
uint32 IsLSPreventUpgradeGPEnabled(
  [out] boolean Enabled
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Habilitado* \[ out\]
</dt> <dd>

Valor booliana que indica se a configuração de política "impedir a atualização de licença" está habilitada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, ele retornará zero. Se o método não for bem-sucedido, ele retornará um valor diferente de zero. Para ver uma lista de códigos de erro, consulte Serviços de Área de Trabalho Remota códigos de erro do provedor [WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Comentários

Você deve ser um membro do grupo Administradores para chamar esse método.

Se a configuração de política "impedir a atualização de licença" estiver habilitada, o servidor de licença emitirá apenas uma CAL de RDS temporária para o cliente se uma CAL de RDS apropriada para o servidor Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) não estiver disponível.

A configuração de política está localizada no seguinte nó do editor de política de grupo local:

Configuração do \\ computador Modelos Administrativos Windows licenciamento \\ \\ TS dos Serviços de Terminal de \\ Componentes do Computador

arquivos Managed Object Format (MOF) contêm as definições para classes WMI (Instrumentação de Gerenciamento de Windows). Os arquivos MOF não são instalados como parte do Microsoft Windows Software Development Kit (SDK). Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, [consulte Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                            |
| Namespace<br/>                | Raiz\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ TSLicenseServer**](win32-tslicenseserver.md)
</dt> </dl>

 

