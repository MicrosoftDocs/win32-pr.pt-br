---
description: As \_ constantes de sinalizador de bit LINEADDRESSMODE descrevem várias maneiras de identificar um endereço em um dispositivo de linha.
ms.assetid: f0f132a0-2e8e-478f-909b-c100aa360daa
title: Constantes de LINEADDRESSMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e5e926772c82a36865c7f3b95c1ca1321db5682
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810460"
---
# <a name="lineaddressmode_-constants"></a>\_Constantes LINEADDRESSMODE

As constantes de sinalizador de bit **LINEADDRESSMODE \_** descrevem várias maneiras de identificar um endereço em um dispositivo de linha.

<dl> <dt>

<span id="LINEADDRESSMODE_ADDRESSID"></span><span id="lineaddressmode_addressid"></span>**LINEADDRESSMODE \_ AddressID**
</dt> <dd> <dl> <dt>



O endereço é especificado com um pequeno inteiro no intervalo de 0 a *dwNumAddresses* menos um, em que *dwNumAddresses* é o valor nos recursos do dispositivo da linha.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSMODE_DIALABLEADDR"></span><span id="lineaddressmode_dialableaddr"></span>**LINEADDRESSMODE \_ DIALABLEADDR**
</dt> <dd> <dl> <dt>



O endereço é especificado por meio de seu número de telefone.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Os 16 bits de ordem superior podem ser atribuídos para extensões específicas do dispositivo. Os 16 bits de ordem inferior são reservados.

Essa constante é usada para selecionar um endereço em uma linha na qual uma chamada deve ser originada. O modelo usual selecionaria o endereço por meio de seu identificador de endereço. Identificadores de endereço são o mecanismo usado para identificar endereços em toda a TAPI. No entanto, em alguns ambientes, ao fazer uma chamada, geralmente é mais prático identificar o endereço de origem de uma chamada por número de telefone em vez de pelo identificador de endereço. Um exemplo é a possível modelagem de um grande número de estações (terceiros) no comutador por meio de um dispositivo de linha com muitos endereços. A linha representa o conjunto de todas as estações e cada estação é mapeada para um endereço com seu próprio número de telefone principal e identificador de endereço.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| parâmetro<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




