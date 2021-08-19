---
title: Método IsLSonDC da classe Win32_TSLicenseServer
description: Recupera se Área de Trabalho Remota licenciamento (Licenciamento RD) está instalado em um controlador de domínio.
ms.assetid: 43345dc8-c8b6-4c41-b26d-781293d07516
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método IsLSonDC
- Método IsLSonDC Serviços de Área de Trabalho Remota, classe Win32_TSLicenseServer
- Classe Win32_TSLicenseServer Serviços de Área de Trabalho Remota, método IsLSonDC
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsLSonDC
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e7f0cfcb97cf479de6effa6781a3d96cd7e39666f4cb0fb3fb54399a974bc0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000666"
---
# <a name="islsondc-method-of-the-win32_tslicenseserver-class"></a>Método IsLSonDC da classe Win32 \_ TSLicenseServer

Recupera se Área de Trabalho Remota licenciamento (Licenciamento RD) está instalado em um controlador de domínio.

## <a name="syntax"></a>Sintaxe


```mof
uint32 IsLSonDC(
  [out] boolean OnDC
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*OnDC* \[ fora\]
</dt> <dd>

Valor booliano que indica se o Licenciamento RD está instalado em um controlador de domínio.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método tiver sucesso, ele retornará zero. Se o método não for bem-sucedido, ele retornará um valor diferente de zero. Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Comentários

Você deve ser um membro do grupo Administradores para chamar esse método.

os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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

 

