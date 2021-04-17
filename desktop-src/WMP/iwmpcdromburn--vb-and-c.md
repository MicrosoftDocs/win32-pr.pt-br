---
title: Interface IWMPCdromBurn (VB e C) (WMP. h)
description: Fornece propriedades e métodos para gerenciar a criação de CDs de áudio.
ms.assetid: d98b243d-d6c2-4d85-8d5a-de49c62d0acf
keywords:
- IWMPCdromBurn (VB e C) interface do Windows Media Player
- IWMPCdromBurn (VB e C) interface do Windows Media Player, descrito
topic_type:
- apiref
api_name:
- IWMPCdromBurn (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2fe21a20194f57e4a8b52a3ba05032a07cb31f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759697"
---
# <a name="iwmpcdromburn-vb-and-c-interface"></a>Interface IWMPCdromBurn (VB e C#)

Fornece propriedades e métodos para gerenciar a criação de CDs de áudio.

## <a name="members"></a>Membros

A interface **IWMPCdromBurn (VB e C#)** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A interface **IWMPCdromBurn (VB e C#)** tem esses métodos.



| Método                                                                             | Descrição                                                              |
|:-----------------------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [**erase**](wmplibiwmpcdromburn-iwmpcdromburn-erase--vb-and-c.md)                 | Apaga o CD atual.<br/>                                        |
| [**getItemInfo**](wmplibiwmpcdromburn-iwmpcdromburn-getiteminfo-iwmpcdromburn.md) | Recupera o valor do atributo especificado para o CD.<br/>    |
| [**isAvailable**](wmplibiwmpcdromburn-iwmpcdromburn-isavailable--vb-and-c.md)     | Fornece informações sobre a unidade de CD e a mídia.<br/>            |
| [**refreshStatus**](wmplibiwmpcdromburn-iwmpcdromburn-refreshstatus--vb-and-c.md) | Atualiza as informações de status da lista de reprodução de gravação atual.<br/> |
| [**startBurn**](wmplibiwmpcdromburn-iwmpcdromburn-startburn--vb-and-c.md)         | Grava o CD.<br/>                                                 |
| [**stopBurn**](wmplibiwmpcdromburn-iwmpcdromburn-stopburn-iwmpcdromburn.md)       | Interrompe o processo de gravação de CD.<br/>                                 |



 

### <a name="properties"></a>Propriedades

A interface **IWMPCdromBurn (VB e C#)** tem essas propriedades.



| Propriedade                                                                                    | Tipo de acesso          | Descrição                                                                 |
|:--------------------------------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------|
| [**burnFormat**](wmplibiwmpcdromburn-iwmpcdromburn-burnformat--vb-and-c.md)<br/>     | Somente leitura<br/> | Obtém um valor que indica o tipo de CD a ser gravado.<br/>              |
| [**burnPlaylist**](wmplibiwmpcdromburn-iwmpcdromburn-burnplaylist--vb-and-c.md)<br/> | Somente leitura<br/> | Obtém a lista de reprodução atual para gravar no CD.<br/>                     |
| [**burnProgress**](wmplibiwmpcdromburn-iwmpcdromburn-burnprogress--vb-and-c.md)<br/> | Somente leitura<br/> | Obtém o progresso da gravação do CD como porcentagem concluída.<br/>                |
| [**gravarstate**](wmplibiwmpcdromburn-iwmpcdromburn-burnstate--vb-and-c.md)<br/>       | Somente leitura<br/> | Obtém um valor de enumeração que indica o estado de gravação atual.<br/> |
| [**chamada**](wmplibiwmpcdromburn-iwmpcdromburn-label--vb-and-c.md)<br/>               | Somente leitura<br/> | Obtém a cadeia de caracteres do rótulo do volume do CD.<br/>                                 |



 

Obtenha uma interface **IWMPCdromBurn** convertendo a interface **IWMPCdrom** do CD que você deseja gravar.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interfaces para Visual Basic .NET e C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> </dl>

 

 





