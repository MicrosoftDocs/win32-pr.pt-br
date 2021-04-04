---
title: Método CreateTSCGroup da classe Win32_TSLicenseServer
description: O CreateTSCGroup não está mais disponível para uso a partir do Windows Server 2012.
ms.assetid: 31751da7-263b-4911-a328-246457a606f0
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método CreateTSCGroup
- Método CreateTSCGroup Serviços de Área de Trabalho Remota, classe Win32_TSLicenseServer
- Classe Win32_TSLicenseServer Serviços de Área de Trabalho Remota, método CreateTSCGroup
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.CreateTSCGroup
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63f10db61cb02ece09d168cb462e31246e498494
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824234"
---
# <a name="createtscgroup-method-of-the-win32_tslicenseserver-class"></a>Método CreateTSCGroup da classe Win32 \_ TSLicenseServer

\[O **CreateTSCGroup** não está mais disponível para uso a partir do Windows Server 2012.\]

Não há suporte para o método.

**Windows server 2008 R2 e Windows server 2008:** Cria o grupo local computadores Terminal Server no Área de Trabalho Remota servidor de licença.

## <a name="syntax"></a>Sintaxe


```mof
uint32 CreateTSCGroup();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna o **WBEM \_ E \_ não \_ tem suporte**.

**Windows server 2008 R2 e Windows server 2008:** Se o método tiver sucesso, ele retornará zero. Se o método não for bem-sucedido, ele retornará um valor diferente de zero. Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Comentários

Você deve ser um membro do grupo Administradores para chamar esse método.

Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                            |
| Fim do suporte do cliente<br/>    | Nenhum compatível<br/>                                                                 |
| Fim do suporte do servidor<br/>    | Windows Server 2008 R2<br/>                                                         |
| Namespace<br/>                | Raiz\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_TSLicenseServer Win32**](win32-tslicenseserver.md)
</dt> <dt>

[**IsTSCGroupPresent**](istscgrouppresent-win32-tslicenseserver.md)
</dt> </dl>

 

