---
title: Tipos de recursos (WinUser. h)
description: A seguir estão os tipos de recursos predefinidos.
ms.assetid: 8d27f79a-8165-4565-a975-f25b2344efdc
topic_type:
- apiref
api_name:
- RT_ACCELERATOR
- RT_ANICURSOR
- RT_ANIICON
- RT_BITMAP
- RT_CURSOR
- RT_DIALOG
- RT_DLGINCLUDE
- RT_FONT
- RT_FONTDIR
- RT_GROUP_CURSOR
- RT_GROUP_ICON
- RT_HTML
- RT_ICON
- RT_MANIFEST
- RT_MENU
- RT_MESSAGETABLE
- RT_PLUGPLAY
- RT_RCDATA
- RT_STRING
- RT_VERSION
- RT_VXD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6cd11856ea1e500425a2d9767dd144ebc9f5e31f583cd07961376aba0ef585b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117687150"
---
# <a name="resource-types"></a>Tipos de recurso

A seguir estão os tipos de recursos predefinidos.



| Constante/valor                                                                                                                                                                                                                                                           | Descrição                                                                                                                                                                                                                                                                                      |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RT_ACCELERATOR"></span><span id="rt_accelerator"></span><dl> <dt>**RT \_ ACELERAdor**</dt> <dt>MAKEINTRESOURCE (9)</dt> </dl>                                 | Tabela de acelerador.<br/>                                                                                                                                                                                                                                                                    |
| <span id="RT_ANICURSOR"></span><span id="rt_anicursor"></span><dl> <dt>**RT \_ ANICURSOR**</dt> <dt>MAKEINTRESOURCE (21)</dt> </dl>                                      | Cursor animado.<br/>                                                                                                                                                                                                                                                                      |
| <span id="RT_ANIICON"></span><span id="rt_aniicon"></span><dl> <dt>**RT \_ ANIICON**</dt> <dt>MAKEINTRESOURCE (22)</dt> </dl>                                            | Ícone animado.<br/>                                                                                                                                                                                                                                                                        |
| <span id="RT_BITMAP"></span><span id="rt_bitmap"></span><dl> <dt>**RT \_**</dt> <dt>MAKEINTRESOURCE de bitmap (2)</dt> </dl>                                                | Recurso de bitmap.<br/>                                                                                                                                                                                                                                                                      |
| <span id="RT_CURSOR"></span><span id="rt_cursor"></span><dl> <dt>**RT \_**</dt> <dt>MAKEINTRESOURCE do cursor (1)</dt> </dl>                                                | Recurso de cursor dependente de hardware.<br/>                                                                                                                                                                                                                                                   |
| <span id="RT_DIALOG"></span><span id="rt_dialog"></span><dl> <dt>**RT \_**</dt> <dt>MAKEINTRESOURCE de diálogo (5)</dt> </dl>                                                | Caixa de diálogo.<br/>                                                                                                                                                                                                                                                                           |
| <span id="RT_DLGINCLUDE"></span><span id="rt_dlginclude"></span><dl> <dt>**RT \_ DLGINCLUDE**</dt> <dt>MAKEINTRESOURCE (17)</dt> </dl>                                   | Permite que uma ferramenta de edição de recursos associe uma cadeia de caracteres a um arquivo. rc. Normalmente, a cadeia de caracteres é o nome do arquivo de cabeçalho que fornece nomes simbólicos. O compilador de recurso analisa a cadeia de caracteres, mas, caso contrário, ignora o valor. Por exemplo, <br/> `1 DLGINCLUDE "MyFile.h"`<br/> |
| <span id="RT_FONT"></span><span id="rt_font"></span><dl> <dt>**RT \_**</dt> <dt>MAKEINTRESOURCE da fonte (8)</dt> </dl>                                                      | Recurso de fonte.<br/>                                                                                                                                                                                                                                                                        |
| <span id="RT_FONTDIR"></span><span id="rt_fontdir"></span><dl> <dt>**RT \_ FONTDIR**</dt> <dt>MAKEINTRESOURCE (7)</dt> </dl>                                             | Recurso de diretório de fontes.<br/>                                                                                                                                                                                                                                                              |
| <span id="RT_GROUP_CURSOR"></span><span id="rt_group_cursor"></span><dl> <dt>**RT \_ \_**</dt> <dt>MAKEINTRESOURCE do cursor de grupo ((ULONG \_ PTR) ( \_ cursor RT) + 11)</dt> </dl> | Recurso de cursor independente de hardware.<br/>                                                                                                                                                                                                                                                 |
| <span id="RT_GROUP_ICON"></span><span id="rt_group_icon"></span><dl> <dt>**RT \_ \_Ícone de grupo**</dt> <dt>MAKEINTRESOURCE ((ULONG \_ PTR) (ícone de RT \_ ) + 11)</dt> </dl>         | Recurso de ícone independente de hardware.<br/>                                                                                                                                                                                                                                                   |
| <span id="RT_HTML"></span><span id="rt_html"></span><dl> <dt>**RT \_ MAKEINTRESOURCE HTML**</dt> <dt>(23)</dt> </dl>                                                     | Recurso HTML.<br/>                                                                                                                                                                                                                                                                        |
| <span id="RT_ICON"></span><span id="rt_icon"></span><dl> <dt>**RT \_ ÍCONE**</dt> <dt>MAKEINTRESOURCE (3)</dt> </dl>                                                      | Recurso de ícone dependente de hardware.<br/>                                                                                                                                                                                                                                                     |
| <span id="RT_MANIFEST"></span><span id="rt_manifest"></span><dl> <dt>**RT \_**</dt> <dt>MAKEINTRESOURCE de manifesto (24)</dt> </dl>                                         | Manifesto do assembly lado a lado.<br/>                                                                                                                                                                                                                                                       |
| <span id="RT_MENU"></span><span id="rt_menu"></span><dl> <dt>**RT \_ MENU**</dt> <dt>MAKEINTRESOURCE (4)</dt> </dl>                                                      | Recurso de menu.<br/>                                                                                                                                                                                                                                                                        |
| <span id="RT_MESSAGETABLE"></span><span id="rt_messagetable"></span><dl> <dt>**RT \_ MAKEINTRESOURCE de mensagens da mensagem**</dt> <dt>(11)</dt> </dl>                             | Entrada da tabela de mensagens.<br/>                                                                                                                                                                                                                                                                  |
| <span id="RT_PLUGPLAY"></span><span id="rt_plugplay"></span><dl> <dt>**RT \_ PLUGPLAY**</dt> <dt>MAKEINTRESOURCE (19)</dt> </dl>                                         | Plug and Play recurso.<br/>                                                                                                                                                                                                                                                               |
| <span id="RT_RCDATA"></span><span id="rt_rcdata"></span><dl> <dt>**RT \_ RCDATA**</dt> <dt>MAKEINTRESOURCE (10)</dt> </dl>                                               | Recurso definido pelo aplicativo (dados brutos).<br/>                                                                                                                                                                                                                                              |
| <span id="RT_STRING"></span><span id="rt_string"></span><dl> <dt>**RT \_ Cadeia de caracteres**</dt> <dt>MAKEINTRESOURCE (6)</dt> </dl>                                                | Entrada de tabela de cadeia de caracteres.<br/>                                                                                                                                                                                                                                                                   |
| <span id="RT_VERSION"></span><span id="rt_version"></span><dl> <dt>**RT \_ VERSÃO**</dt> <dt>MAKEINTRESOURCE (16)</dt> </dl>                                            | Recurso de versão.<br/>                                                                                                                                                                                                                                                                     |
| <span id="RT_VXD"></span><span id="rt_vxd"></span><dl> <dt>**RT \_ VXD**</dt> <dt>MAKEINTRESOURCE (20)</dt> </dl>                                                        | VXD.<br/>                                                                                                                                                                                                                                                                                  |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|--------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>WinUser. h</dt> </dl> |



 

 





