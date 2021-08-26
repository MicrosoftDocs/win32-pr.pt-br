---
description: Construtor de CPosPassThru. CPosPassThru-método de construtor.
ms.assetid: b258401c-158b-4eb8-8736-1e1ad9a8403a
title: Construtor CPosPassThru. CPosPassThru
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.CPosPassThru
api_type:
- COM
api_location: ''
ms.openlocfilehash: ec75218f43edcf6c3c2c6298eba7c886cdd04879485bf41f20951cba1f9c4935
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108316"
---
# <a name="cpospassthrucpospassthru-constructor"></a>Construtor CPosPassThru. CPosPassThru

Método de construtor.

## <a name="syntax"></a>Sintaxe


```C++
CPosPassThru(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr,
         IPin      *pPin,
                   
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pName* 
</dt> <dd>

Ponteiro para o nome do objeto, para fins de depuração. Aloque esse parâmetro na memória estática.

</dd> <dt>

*pUnk* 
</dt> <dd>

Ponteiro para o proprietário deste objeto. Se o objeto for agregado, passe um ponteiro para a interface **IUnknown** do objeto de agregação. Caso contrário, defina esse parâmetro como **NULL**.

</dd> <dt>

*phr* 
</dt> <dd>

Ponteiro para um valor **HRESULT** . Ignorado.

</dd> <dt>

*pPin* 
</dt> <dd>

Ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do PIN de entrada do filtro.

</dd> <dt>

 
</dt> <dd></dd> </dl>

 

 



