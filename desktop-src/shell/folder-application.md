---
description: Contém o objeto de aplicativo da pasta.
ms.assetid: 1dba83eb-1af6-42d9-b2c9-ab7767888efe
title: Propriedade Folder. Application (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.Application
api_type:
- COM
api_location:
- Shldisp.h
ms.openlocfilehash: 13a6a90dd324498c332f7bf580ff5ec987a0c5b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457204"
---
# <a name="folderapplication-property"></a>Propriedade Folder. Application

Contém o objeto de aplicativo da pasta.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
Application = Folder.Application
```



## <a name="property-value"></a>Valor da propriedade

Uma referência de objeto para o objeto de aplicativo.

## <a name="remarks"></a>Comentários

A propriedade **Application** retorna o objeto Automation com suporte do aplicativo que contém o controle WebBrowser, se esse objeto estiver acessível. Caso contrário, essa propriedade retornará o objeto de automação do controle WebBrowser.

Use essa propriedade com os comandos **set** e **CreateObject** ou com o comando **GetObject** para criar e manipular uma instância do aplicativo Internet Explorer.

> [!Note]  
> Nem todos os métodos são implementados para todas as pastas. Por exemplo, o método [**ParseName**](folder-parsename.md) não é implementado para a pasta do painel de controle ( \_ controles CSIDL). Se você tentar chamar um método não implementado, um erro 0x800A01BD (decimal 445) será gerado.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]<br/>                 |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Cabeçalho<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl> |



 

 




