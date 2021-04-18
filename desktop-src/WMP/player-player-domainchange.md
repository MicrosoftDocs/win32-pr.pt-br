---
title: Evento Player. DomainChange
description: O evento DomainChange ocorre quando o domínio do DVD é alterado. | Evento Player. DomainChange
ms.assetid: 01965492-276e-4d30-99eb-767e0776b423
keywords:
- Evento DomainChange do Windows Media Player
- Evento DomainChange Windows Media Player, classe Player
- Classe de jogador Windows Media Player, evento DomainChange
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
ms.openlocfilehash: fa9637913451aa5bba937906130899c46e0bd34d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105814070"
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

## <a name="return-value"></a>Retornar valor

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

O valor dos parâmetros de evento é especificado pelo Windows Media Player e pode ser acessado ou transmitido para um método em um arquivo JScript importado usando o nome de parâmetro fornecido. Esse nome de parâmetro deve ser digitado exatamente como mostrado, incluindo a capitalização.

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

 

 





