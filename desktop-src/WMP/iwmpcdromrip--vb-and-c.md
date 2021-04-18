---
title: Interface IWMPCdromRip (VB e C) (WMP. h)
description: Fornece propriedades e métodos para gerenciar a cópia, ou copiar, faixas de um CD de áudio. copiar um CD usando a interface IWMPCdromRip tem o mesmo efeito que copiar música usando a interface do usuário do Windows Media Player.
ms.assetid: d7fbfc68-61b5-45bf-8df5-e3125a51a4d8
keywords:
- IWMPCdromRip (VB e C) interface do Windows Media Player
- IWMPCdromRip (VB e C) interface do Windows Media Player, descrito
topic_type:
- apiref
api_name:
- IWMPCdromRip (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d069fd8bd727d6a2a380c2ef29ce7c086db88d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779994"
---
# <a name="iwmpcdromrip-vb-and-c-interface"></a>Interface IWMPCdromRip (VB e C#)

Fornece propriedades e métodos para gerenciar a cópia, ou *copiar*, faixas de um CD de áudio.

Copiar um CD usando a interface **IWMPCdromRip** tem o mesmo efeito que copiar música usando a interface do usuário do Windows Media Player. O conteúdo copiado é adicionado automaticamente à biblioteca de acordo com as preferências do usuário. Para obter mais informações sobre as preferências do usuário para a cópia de CD, consulte "copiando música de CDs" na ajuda do Windows Media Player.

A interface **IWMPCdromRip** expõe as propriedades a seguir.

## <a name="members"></a>Membros

A interface **IWMPCdromRip (VB e C#)** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A interface **IWMPCdromRip (VB e C#)** tem esses métodos.



| Método                                                                 | Descrição                              |
|:-----------------------------------------------------------------------|:-----------------------------------------|
| [**startRip**](wmplibiwmpcdromrip-iwmpcdromrip-startrip--vb-and-c.md) | Rips o CD.<br/>                  |
| [**stopRip**](wmplibiwmpcdromrip-iwmpcdromrip-stoprip--vb-and-c.md)   | Interrompe o processo de cópia de CD.<br/> |



 

### <a name="properties"></a>Propriedades

A interface **IWMPCdromRip (VB e C#)** tem essas propriedades.



| Propriedade                                                                                | Tipo de acesso          | Descrição                                                                                   |
|:----------------------------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------|
| [**ripProgress**](wmplibiwmpcdromrip-iwmpcdromrip-ripprogress--vb-and-c.md)<br/> | Somente leitura<br/> | Obtém o progresso da cópia do CD como porcentagem concluída.<br/>                                  |
| [**ripState**](wmplibiwmpcdromrip-iwmpcdromrip-ripstate--vb-and-c.md)<br/>       | Somente leitura<br/> | Obtém um valor de enumeração que indica o estado atual do processo de cópia de CDs.<br/> |



 

Obtenha uma interface **IWMPCdromRip** convertendo a interface **IWMPCdrom** do CD que você deseja copiar.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interfaces para Visual Basic .NET e C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Copiando um CD**](ripping-a-cd.md)
</dt> </dl>

 

 





