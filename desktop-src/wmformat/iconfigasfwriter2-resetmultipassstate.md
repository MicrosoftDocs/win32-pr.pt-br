---
title: Método IConfigAsfWriter2 ResetMultiPassState
description: O método ResetMultiPassState redefine o filtro quando uma passagem de codificação de pré-processamento é cancelada antes de ser concluída.
ms.assetid: b6687af7-f3cd-4e92-9c76-dddff9063fa0
keywords:
- Formato de mídia do windows do método ResetMultiPassState
- Formato de mídia do método ResetMultiPassState, interface IConfigAsfWriter2
- Formato de mídia da interface IConfigAsfWriter2 , método ResetMultiPassState
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.ResetMultiPassState
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1f10563ed716b6b33258fe57ff8129bff78b401170db1512566015d0b05d54dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839866"
---
# <a name="iconfigasfwriter2resetmultipassstate-method"></a>Método IConfigAsfWriter2::ResetMultiPassState

O **método ResetMultiPassState** redefine o filtro quando uma passagem de codificação de pré-processamento é cancelada antes de ser concluída.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ResetMultiPassState();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT.** Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                                         | Descrição                                       |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                | O método foi bem-sucedido.<br/>                  |
| <dl> <dt>**VFW \_ E \_ NÃO INTERROMPIDO \_**</dt> </dl> | O filtro não estava em um estado parado.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método deve ser chamado para redefinir o estado interno do filtro sempre que uma passagem de codificação de pré-processamento for cancelada antes que o filtro tenha recebido um evento **EC \_ PREPROCESS \_ COMPLETE.** Não é necessário chamar esse método se a passagem de codificação de pré-processamento for concluída sem erros.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IConfigAsfWriter2 Interface**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))
</dt> </dl>

 

