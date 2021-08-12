---
title: Interface IWMPCdromBurn (VB e C) (WMP. h)
description: Fornece propriedades e métodos para gerenciar a criação de CDs de áudio.
ms.assetid: d98b243d-d6c2-4d85-8d5a-de49c62d0acf
keywords:
- Windows Media Player de interface IWMPCdromBurn (VB e C)
- Windows Media Player de interface IWMPCdromBurn (VB e C), descrita
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
ms.openlocfilehash: 7731d5491e683c2a5d2e577c41dc96264c90f0d070538405d0fa3c3ea7283a0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118575954"
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

[**Interfaces para Visual Basic .net e C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> </dl>

 

 





