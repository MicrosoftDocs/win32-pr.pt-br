---
title: Configurações. enableErrorDialogs
description: A propriedade enableErrorDialogs especifica ou recupera um valor que indica se as caixas de diálogo de erro são mostradas automaticamente.
ms.assetid: 16b10bea-4b3e-469f-a903-02f19ffcdf31
keywords:
- Configurações. enableErrorDialogs Windows Media Player
topic_type:
- apiref
api_name:
- Settings.enableErrorDialogs
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa786606a97edcfca22512dd0b3188a06a7851f8bab2401e139d7ead2c3495ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118569368"
---
# <a name="settingsenableerrordialogs"></a>Configurações. enableErrorDialogs

A propriedade **enableErrorDialogs** especifica ou recupera um valor que indica se as caixas de diálogo de erro são mostradas automaticamente.

## <a name="syntax"></a>Sintaxe

Player. Settings. enableErrorDialogs

## <a name="possible-values"></a>Valores possíveis

Esta propriedade é um **booliano** de leitura/gravação.



| Valor | Descrição                                     |
|-------|-------------------------------------------------|
| true  | Padrão. As caixas de diálogo de erro são mostradas automaticamente. |
| false | As caixas de diálogo de erro não são mostradas automaticamente.      |



 

## <a name="remarks"></a>Comentários

Essa propriedade exibe um comportamento específico para instâncias remotas do controle do Player. para obter mais informações, consulte [comunicação remota do controle de Windows Media Player](remoting-the-windows-media-player-control.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Configurações Objeto**](settings-object.md)
</dt> </dl>

 

 





