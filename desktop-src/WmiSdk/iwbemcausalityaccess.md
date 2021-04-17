---
description: Controla as solicitações filhas que são geradas a partir de uma solicitação pai.
ms.assetid: e1d98eae-6fc1-489b-aa8b-2e86bac5c65a
ms.tgt_platform: multiple
title: Interface IWbemCausalityAccess (Wbemint. h)
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
ms.openlocfilehash: db4c7a76b04b659cd467f7a4a7a9a8c1ba42721f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748862"
---
# <a name="iwbemcausalityaccess-interface"></a>Interface IWbemCausalityAccess

A interface **IWbemCausalityAccess** mantém o controle das solicitações filho que são geradas a partir de uma solicitação pai. Você pode obter um objeto **IWbemCausalityAccess** usando uma interface de consulta (QI) para [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext). Cada solicitação é identificada por um GUID (identificador global exclusivo) e pode ter uma solicitação pai ou pode ser uma solicitação superior. Um GUID é um número de bits de 128 exclusivo. Por exemplo, 5b2fc63a-8af4-44cb-960C-aefdced908d6.

## <a name="members"></a>Membros

A interface **IWbemCausalityAccess** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IWbemCausalityAccess** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IWbemCausalityAccess** tem esses métodos.



| Método                                                    | Descrição                                                                                                                                                             |
|:----------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Getsolicitid**](iwbemcausalityaccess-getrequestid.md) | Retorna um identificador GUID exclusivo para uma solicitação.<br/>                                                                                                              |
| [**IsChildOf**](iwbemcausalityaccess-ischildof.md)       | Determina se uma solicitação é um filho de uma solicitação pai especificada. Uma solicitação pai pode ter várias solicitações filho, cada uma identificada por um valor GUID exclusivo.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Wbemint. h</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>Fastprox.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[API COM para WMI](com-api-for-wmi.md)
</dt> </dl>

 

