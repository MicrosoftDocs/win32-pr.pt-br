---
description: O método SetGPRM define o registro de parâmetro geral especificado como o valor especificado.
ms.assetid: ded28f2a-5e40-4f76-9ed4-de10296529e1
title: Método SetGPRM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c217f0235ca5b055e20102f553e9e23f5b93e6dd9c3d74db560584690a669ea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078856"
---
# <a name="setgprm-method"></a>Método SetGPRM

> [!Note]  
> esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O `SetGPRM` método define o registro de parâmetro geral especificado para o valor especificado.

``` syntax
MSWebDVD.SetGPRM(iIndex, nValue)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*
</dt> <dd>

Especifica o registro de parâmetro geral a ser definido como um inteiro. O valor inteiro deve variar de 0 a 15.

</dd> <dt>

<span id="nValue"></span><span id="nvalue"></span><span id="NVALUE"></span>*nvalor*
</dt> <dd>

Especifica o novo valor para o registro como um inteiro.

</dd> </dl>

## <a name="remarks"></a>Comentários

Registros de parâmetro gerais, ou GPRMs, são registros de 16 bits que cada disco pode usar de maneiras exclusivas para o armazenamento temporário de dados. Um aplicativo de Player não precisa acessar esses registros para qualquer reprodução padrão ou controle de navegação usando o objeto **MSWebDVD** . Esse método é fornecido para aplicativos de Player que implementam a funcionalidade avançada. Não tente modificar o GPRMs diretamente, a menos que você tenha um conhecimento completo sobre a especificação de DVD e as maneiras em que os GPRMs são usados no disco específico a ser reproduzido. A alteração desses valores pode resultar em um comportamento imprevisível.

 

 



