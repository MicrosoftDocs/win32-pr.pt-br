---
title: Evento Player. DomainChange
description: O evento DomainChange ocorre quando o domínio do DVD é alterado. | Evento Player. DomainChange
ms.assetid: 01965492-276e-4d30-99eb-767e0776b423
keywords:
- Windows Media Player de eventos DomainChange
- Windows Media Player de eventos DomainChange, classe Player
- classe de jogador Windows Media Player, evento DomainChange
topic_type:
- apiref
api_name:
- Player.DomainChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f6d70c6a3c2ac2d29c03e6d0518b5e7341f988f41e1bf2f5bb84a7de9f83f68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995906"
---
# <a name="playerdomainchange-event"></a>Evento Player. DomainChange

O evento **DomainChange** ocorre quando o domínio do DVD é alterado.

## <a name="syntax"></a>Sintaxe


```JScript
Player.DomainChange(
  strDomain
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*strDomain* 
</dt> <dd>

**Cadeia de caracteres** que indica o novo domínio. Contém um dos seguintes valores.



| String            | Descrição                                                          |
|-------------------|----------------------------------------------------------------------|
| firstplay         | Executando a inicialização padrão de um disco de DVD.                     |
| videoManagerMenu  | Exibindo menus para o disco inteiro. Também conhecido como menu raiz ou topMenu. |
| videoTitleSetMenu | Exibindo menus para o conjunto de títulos atual. Também conhecido como titleMenu.     |
| título             | Exibindo o título atual.                                        |
| parar              | O navegador de DVD está no domínio de parada de DVD.                         |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

o valor dos parâmetros de evento é especificado por Windows Media Player e pode ser acessado ou passado para um método em um arquivo de JScript importado usando o nome de parâmetro fornecido. Esse nome de parâmetro deve ser digitado exatamente como mostrado, incluindo a capitalização.

**Windows Media Player 10 Mobile:** Não há suporte para esse evento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player para Windows XP ou posterior.<br/>                           |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de DVD**](dvd-object.md)
</dt> <dt>

[**Objeto de jogador**](player-object.md)
</dt> </dl>

 

 





