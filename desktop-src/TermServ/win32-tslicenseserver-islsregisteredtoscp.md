---
title: Método IsLSRegisteredToSCP da classe Win32_TSLicenseServer
description: Recupera se o servidor Área de Trabalho Remota licença está registrado como um ponto de conexão de serviço no Active Directory Domain Services.
ms.assetid: 013C3711-7C55-4DB4-9229-C3C60E751EF2
ms.tgt_platform: multiple
keywords:
- Método IsLSRegisteredToSCP Serviços de Área de Trabalho Remota
- Método IsLSRegisteredToSCP Serviços de Área de Trabalho Remota , Win32_TSLicenseServer classe
- Win32_TSLicenseServer classe Serviços de Área de Trabalho Remota , método IsLSRegisteredToSCP
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsLSRegisteredToSCP
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a47ca9eadbdbaaba49311b212e83528ee391387e7aca1512a1ab0001a2bbae8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058334"
---
# <a name="islsregisteredtoscp-method-of-the-win32_tslicenseserver-class"></a>Método IsLSRegisteredToSCP da classe \_ Win32 TSLicenseServer

Recupera se o servidor Área de Trabalho Remota licença está registrado como um ponto de conexão de serviço no Active Directory Domain Services.

## <a name="syntax"></a>Sintaxe


```mof
uint32 IsLSRegisteredToSCP(
  [out] boolean Registered
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Registrado* \[ out\]
</dt> <dd>

Valor booliana que indica se o servidor Área de Trabalho Remota licença está registrado como um ponto de conexão de serviço no Active Directory Domain Services.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, ele retornará zero. Se o método não for bem-sucedido, ele retornará um valor diferente de zero. Para ver uma lista de códigos de erro, consulte Serviços de Área de Trabalho Remota códigos de erro do provedor [WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Comentários

Você deve ser um membro do grupo Administradores para chamar esse método.

arquivos Managed Object Format (MOF) contêm as definições para classes WMI (Instrumentação de Gerenciamento de Windows). Os arquivos MOF não são instalados como parte do Microsoft Windows Software Development Kit (SDK). Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, [consulte Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2<br/>                                                         |
| Namespace<br/>                | Raiz\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ TSLicenseServer**](win32-tslicenseserver.md)
</dt> </dl>

 

