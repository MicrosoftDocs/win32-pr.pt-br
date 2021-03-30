---
description: '\\Painel de controle HKCU \\ internacional.'
ms.assetid: e2925d92-19df-42e5-9893-2820f437d3a5
title: AddHijriDate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22a1c4a721af18e0a8994efdd7641581aa01c133
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826234"
---
# <a name="addhijridate"></a>AddHijriDate

**\\Painel de controle HKCU \\ internacional**



| Tipo de dados | Intervalo                      | Valor padrão |
|-----------|----------------------------|---------------|
| REG \_ sz   | *Um valor de ajuste válido* | (Nenhuma)        |



 

## <a name="description"></a>Descrição

Especifica os ajustes para a data dentro do calendário islâmico.

O calendário islâmico é um calendário lunar usado no mundo islâmico. Os meses começam e terminam de acordo com um decree com base na observação da nova lua. É difícil prever com precisão os inícios e finais dos meses, e há variações regionais, de modo que um ajuste entre zero e dois dias seja feito no calendário.

O valor do registro **AddHijriDate** armazena esse valor de ajuste da seguinte maneira.



| Valor          | Significado                                                                                                                                                                                                                               |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AddHijriDate-2 | Subtraia dois dias.                                                                                                                                                                                                                    |
| AddHijriDate   | Subtrair um dia.                                                                                                                                                                                                                     |
| (blank)        | Nenhum ajuste é necessário. (Se a data não tiver sido ajustada, essa entrada não aparecerá no registro. Se a data tiver sido ajustada e restaurada para seu valor original, essa entrada aparecerá no registro sem valor.) |
| AddHijriDate + 1 | Adicionar um dia.                                                                                                                                                                                                                          |
| AddHijriDate + 2 | Adicione dois dias.                                                                                                                                                                                                                         |



 

Essa entrada não existe no Registro por padrão. Você pode adicioná-lo usando o editor do registro Regedit.exe ou usando o método de alteração descrito abaixo.

## <a name="change-method"></a>Alterar Método

Para alterar o valor dessa entrada ou adicioná-la ao registro, primeiro instale os arquivos para os idiomas de script complexo e da direita para a esquerda. No painel de controle, clique em **Opções regionais e de idioma** e clique na guia **idiomas** . Em **suporte a idioma suplementar**, marque a caixa de seleção para **instalar arquivos para scripts complexos e idiomas da direita para a esquerda (incluindo tailandês)**. Clique em **OK**.

Para alterar o valor dessa entrada ou adicioná-la ao registro, no painel de controle, clique em **Opções regionais e de idioma**. No campo **padrões e formatos** , selecione uma localidade que usa o calendário islâmico. Clique no botão **Personalizar** e, em seguida, clique na guia **Data** . Na lista suspensa **Ajustar data do Hijri para:** , selecione o valor apropriado. Clique em **OK** e em **OK** novamente.

## <a name="activation-method"></a>Método de ativação

As alterações nessa entrada feitas por meio do painel de controle entram em vigor imediatamente.

 

 



