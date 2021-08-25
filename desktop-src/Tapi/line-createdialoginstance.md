---
description: A mensagem TSPI LINE CREATEDIALOGINSTANCE faz com que a TAPI crie uma associação entre o provedor de serviços e uma instância da função \_ TUISPI providerGenericDialog em execução no contexto do \_ aplicativo.
ms.assetid: 5a7e34bc-1dc3-40c4-b07e-de5b88cbcd75
title: LINE_CREATEDIALOGINSTANCE mensagem (Tspi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e670a0dbcdde82721e5441b95983d5852e821cc981062947a0d6b76639ad762
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873496"
---
# <a name="line_createdialoginstance-message"></a>Mensagem \_ LINE CREATEDIALOGINSTANCE

A mensagem TSPI **LINE \_ CREATEDIALOGINSTANCE** faz com que a TAPI crie uma associação entre o provedor de serviços e uma instância da função [**TUISPI \_ PROVIDERGenericDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialog) em execução no contexto do aplicativo que invocou a função TSPI assíncrona identificada pelo parâmetro *dwRequestID* da estrutura [**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams) apontada por *lpTUISPICreateDialogInstanceParams*.


```C++
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hProvider* 
</dt> <dd>

O ProviderHandle fornecido ao provedor de serviços como um parâmetro para [**o provedor TSPIEnumDevices. \_**](/windows/win32/api/tspi/nf-tspi-tspi_providerenumdevices)

</dd> <dt>

*lpTUISPICreateDialogInstanceParams* 
</dt> <dd>

Ponteiro para uma [**estrutura TUISPICREATEDIALOGINSTANCEPARAMS.**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams)

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 2.0 ou posterior<br/>                                             |
| Cabeçalho<br/>       | <dl> <dt>Tspi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Provedor \_ TSPIEnumDevices**](/windows/win32/api/tspi/nf-tspi-tspi_providerenumdevices)
</dt> <dt>

[**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams)
</dt> </dl>

 

