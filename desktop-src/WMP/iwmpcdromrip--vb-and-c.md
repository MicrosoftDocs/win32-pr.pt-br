---
title: Interface IWMPCdromRip (VB e C) (WMP. h)
description: fornece propriedades e métodos para gerenciar a cópia, ou copiar, faixas de um cd de áudio. copiar um cd usando a interface IWMPCdromRip tem o mesmo efeito que copiar música usando a interface do usuário Windows Media Player.
ms.assetid: d7fbfc68-61b5-45bf-8df5-e3125a51a4d8
keywords:
- Windows Media Player de interface IWMPCdromRip (VB e C)
- Windows Media Player de interface IWMPCdromRip (VB e C), descrita
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
ms.openlocfilehash: 98a418f71ad8605e81115fa9ef1a45488a6830db94c260ef60aa0d991724d80a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117747932"
---
# <a name="iwmpcdromrip-vb-and-c-interface"></a>Interface IWMPCdromRip (VB e C#)

Fornece propriedades e métodos para gerenciar a cópia, ou *copiar*, faixas de um CD de áudio.

copiar um CD usando a interface **IWMPCdromRip** tem o mesmo efeito que copiar música usando a interface do usuário Windows Media Player. O conteúdo copiado é adicionado automaticamente à biblioteca de acordo com as preferências do usuário. para obter mais informações sobre as preferências do usuário para a cópia de CD, consulte "copiando música de CDs" na ajuda do Windows Media Player.

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

[**Interfaces para Visual Basic .net e C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Copiando um CD**](ripping-a-cd.md)
</dt> </dl>

 

 





