---
description: Mantém o controle das solicitações filho que são geradas de uma solicitação pai.
ms.assetid: e1d98eae-6fc1-489b-aa8b-2e86bac5c65a
ms.tgt_platform: multiple
title: Interface IWbemCausalityAccess (Wbemint.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWbemCausalityAccess
api_type:
- COM
api_location:
- Fastprox.dll
ms.openlocfilehash: a8c71d5b5f59a3b59fe3b639104bfa1fa2dcf9cd35764e37984759827ff7e92b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131388"
---
# <a name="iwbemcausalityaccess-interface"></a>Interface IWbemCausalityAccess

A interface **IWbemCausalityAccess** acompanha as solicitações filho geradas de uma solicitação pai. Você pode obter um **objeto IWbemCausalityAccess** usando uma QI (interface de consulta) para [**IWbemContext.**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) Cada solicitação é identificada por um GUID (Identificador Global Exclusivo) e pode ter uma solicitação pai ou pode ser uma solicitação principal. Um GUID é um número exclusivo de 128 bits. Por exemplo, 5b2fc63a-8af4-44cb-960c-aefdced908d6.

## <a name="members"></a>Membros

A interface **IWbemCausalityAccess** herda da interface [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IWbemCausalityAccess** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IWbemCausalityAccess** tem esses métodos.



| Método                                                    | Descrição                                                                                                                                                             |
|:----------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetRequestId**](iwbemcausalityaccess-getrequestid.md) | Retorna um identificador guid exclusivo para uma solicitação.<br/>                                                                                                              |
| [**IsChildOf**](iwbemcausalityaccess-ischildof.md)       | Determina se uma solicitação é um filho de uma solicitação pai especificada. Uma solicitação pai pode ter várias solicitações filho, cada uma identificada por um valor guid exclusivo.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Wbemint.h</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>Fastprox.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[API COM para WMI](com-api-for-wmi.md)
</dt> </dl>

 

