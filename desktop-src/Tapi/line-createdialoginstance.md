---
description: A mensagem TSPI LINE \_ CREATEDIALOGINSTANCE faz com que a TAPI crie uma associação entre o provedor de serviços e uma instância da \_ função TUISPI providerGenericDialog em execução no contexto do aplicativo.
ms.assetid: 5a7e34bc-1dc3-40c4-b07e-de5b88cbcd75
title: Mensagem de LINE_CREATEDIALOGINSTANCE (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c92088b79bdd085874d14817e6e9652f03c6c00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753538"
---
# <a name="line_createdialoginstance-message"></a>Mensagem de CREATEDIALOGINSTANCE de linha \_

A mensagem **de \_ CREATEDIALOGINSTANCE da linha** TSPI faz com que a TAPI crie uma associação entre o provedor de serviços e uma instância da função [**TUISPI \_ providerGenericDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialog) em execução no contexto do aplicativo que invocou a função TSPI assíncrona identificada pelo parâmetro *DwRequestID* da estrutura [**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams) apontada por *lpTUISPICreateDialogInstanceParams*.


```C++
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hProvider* 
</dt> <dd>

O ProviderHandle fornecido ao provedor de serviços como um parâmetro para [**TSPI \_ providerEnumDevices**](/windows/win32/api/tspi/nf-tspi-tspi_providerenumdevices).

</dd> <dt>

*lpTUISPICreateDialogInstanceParams* 
</dt> <dd>

Ponteiro para uma estrutura [**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams) .

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| parâmetro<br/>       | <dl> <dt>TSPI. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TSPI \_ providerEnumDevices**](/windows/win32/api/tspi/nf-tspi-tspi_providerenumdevices)
</dt> <dt>

[**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams)
</dt> </dl>

 

