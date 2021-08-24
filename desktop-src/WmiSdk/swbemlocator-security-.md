---
description: A propriedade Security do objeto SWbemLocator é usada para ler ou definir as configurações de \_ segurança para um objeto SWbemLocator. Essa propriedade é um objeto SWbemSecurity.
ms.assetid: 75987bef-21ae-4420-b069-afab90499218
ms.tgt_platform: multiple
title: SWbemLocator.Security_ propriedade (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLocator.Security_
- ISWbemLocator.Security_
- ISWbemLocator.get_Security_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 6c5fa2ba102de1135c0019e2dcfb291f55672cabb00cea1c59d8a655f21c882e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955166"
---
# <a name="swbemlocatorsecurity_-property"></a>Propriedade SWbemLocator.Security \_

A **\_ propriedade Security** do [**objeto SWbemLocator**](swbemlocator.md) é usada para ler ou definir as configurações de segurança para um **objeto SWbemLocator.** Essa propriedade é um [**objeto SWbemSecurity.**](swbemsecurity.md)

> [!Note]  
> Definir a **propriedade Security \_** de um objeto [**SWbemLocator**](swbemlocator.md) como **NULL** concede acesso ilimitado a todos o tempo todo. Para obter mais informações, consulte [**SWbemSecurity**](swbemsecurity.md).

 

Para uma explicação dessa sintaxe, consulte [Convenções de documento para a API de Script](document-conventions-for-the-scripting-api.md).

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```VB
SWbemLocator.Security_ As Object
```



## <a name="property-value"></a>Valor da propriedade

## <a name="remarks"></a>Comentários

As propriedades de um **objeto SWbemLocator.Security \_** não têm valores padrão. Se você tentar obter o valor [**de SWbemSecurity.AuthenticationLevel**](swbemsecurity-authenticationlevel.md) ou [**SWbemSecurity.ImpersonationLevel**](swbemsecurity-impersonationlevel.md) em um [**objeto SWbemLocator**](swbemlocator.md) antes de defini-lo, um [wbemErrFailed](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum) resulta em um erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemLocator<br/>                                                          |
| IID<br/>                      | IID \_ ISWbemLocator<br/>                                                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SWbemLocator**](swbemlocator.md)
</dt> <dt>

[Criando um aplicativo ou script WMI](creating-a-wmi-application-or-script.md)
</dt> <dt>

[Executando operações privilegiadas usando o VBScript](executing-privileged-operations-using-vbscript.md)
</dt> <dt>

[Definindo a segurança \_ do processo de aplicativo \_ cliente](setting-client-application-process-security.md)
</dt> <dt>

[**Objeto SWbemSecurity**](swbemsecurity.md)
</dt> <dt>

[Proteger uma conexão WMI remota](securing-a-remote-wmi-connection.md)
</dt> </dl>

 

 




