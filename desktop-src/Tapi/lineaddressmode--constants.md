---
description: As constantes de sinalizador de bits LINEADDRESSMODE descrevem várias maneiras de \_ identificar um endereço em um dispositivo de linha.
ms.assetid: f0f132a0-2e8e-478f-909b-c100aa360daa
title: LINEADDRESSMODE_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4863b79c4527395f6ecb2d28c4d9ef718ff5a7fd99681185ba892bac2b4639ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761858"
---
# <a name="lineaddressmode_-constants"></a>Constantes LINEADDRESSMODE \_

As constantes de sinalizador de bits **LINEADDRESSMODE \_** descrevem várias maneiras de identificar um endereço em um dispositivo de linha.

<dl> <dt>

<span id="LINEADDRESSMODE_ADDRESSID"></span><span id="lineaddressmode_addressid"></span>**LINEADDRESSMODE \_ ADDRESSID**
</dt> <dd> <dl> <dt>



O endereço é especificado com um inteiro pequeno no intervalo de 0 a *dwNumAddresses* menos um, em que *dwNumAddresses é* o valor nas funcionalidades do dispositivo da linha.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSMODE_DIALABLEADDR"></span><span id="lineaddressmode_dialableaddr"></span>**LINEADDRESSMODE \_ DIALABLEADDR**
</dt> <dd> <dl> <dt>



O endereço é especificado por meio de seu número de telefone.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Os 16 bits de ordem alta podem ser atribuídos a extensões específicas do dispositivo. Os 16 bits de ordem baixa são reservados.

Essa constante é usada para selecionar um endereço em uma linha na qual originar uma chamada. O modelo comum selecionaria o endereço por meio de seu identificador de endereço. Identificadores de endereço são o mecanismo usado para identificar endereços em toda a TAPI. No entanto, em alguns ambientes, ao fazer uma chamada, geralmente é mais prático identificar o endereço de origem de uma chamada por número de telefone, em vez de pelo identificador de endereço. Um exemplo é a possível modelagem de um grande número de estações (de terceiros) na opção por meio de um dispositivo de linha com muitos endereços. A linha representa o conjunto de todas as estações e cada estação é mapeada para um endereço com seu próprio número de telefone primário e identificador de endereço.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 2.0 ou posterior<br/>                                             |
| Cabeçalho<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




