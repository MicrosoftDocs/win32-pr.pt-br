---
title: Método IConfigAsfWriter2 ResetMultiPassState
description: O método ResetMultiPassState redefine o filtro quando uma passagem de codificação de pré-processamento é cancelada antes de ser concluída.
ms.assetid: b6687af7-f3cd-4e92-9c76-dddff9063fa0
keywords:
- Formato de mídia do Windows do método ResetMultiPassState
- Método ResetMultiPassState Windows Media Format, interface IConfigAsfWriter2
- Formato de mídia do Windows de interface IConfigAsfWriter2, método ResetMultiPassState
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.ResetMultiPassState
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ed61e4f0517822a602f2bb88c944bba82fa1f943
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366502"
---
# <a name="iconfigasfwriter2resetmultipassstate-method"></a>Método IConfigAsfWriter2:: ResetMultiPassState

O método **ResetMultiPassState** redefine o filtro quando uma passagem de codificação de pré-processamento é cancelada antes de ser concluída.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ResetMultiPassState();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                                         | Descrição                                       |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                | O método foi bem-sucedido.<br/>                  |
| <dl> <dt>**VFW \_ E \_ não \_ parado**</dt> </dl> | O filtro não estava em um estado parado.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método deve ser chamado para redefinir o estado interno do filtro sempre que uma passagem de codificação de pré-processamento for cancelada antes que o filtro tenha recebido um evento de **\_ pré-processamento \_ concluído do EC** . Não é necessário chamar esse método se a passagem de codificação de pré-processamento for concluída sem erros.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IConfigAsfWriter2**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))
</dt> </dl>

 

