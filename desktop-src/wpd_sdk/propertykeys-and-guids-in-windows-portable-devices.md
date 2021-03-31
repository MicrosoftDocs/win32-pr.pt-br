---
description: PROPERTYKEYs e GUIDs em dispositivos portáteis do Windows
ms.assetid: 3f9e9f29-37dd-47b0-997e-de81966efce2
title: PROPERTYKEYs e GUIDs em dispositivos portáteis do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c28cbe76b76eda04852cd1afcbb11b85b0a185d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829083"
---
# <a name="propertykeys-and-guids-in-windows-portable-devices"></a>PROPERTYKEYs e GUIDs em dispositivos portáteis do Windows

Uma propriedade ou comando é identificado por uma estrutura PROPERTYKEY. Uma estrutura PROPERTYKEY é composta de duas partes: um GUID (o membro fmtid) e um DWORD (o membro PID). A parte GUID é usada para indicar a categoria à qual a propriedade ou o comando pertence (ou seja, propriedades relacionadas pertencem à mesma categoria e os comandos relacionados pertencem à mesma categoria; portanto, eles terão o mesmo fmtid). A parte DWORD indica a propriedade ou a ID de comando e é usada para distinguir as propriedades ou comandos individuais dentro de uma categoria de propriedade ou comando (ou seja, os valores de PID para propriedades ou comandos na mesma categoria serão diferentes).

A seção de referência deste documento descreve todos os valores de PROPERTYKEY definidos por WPD; esses valores correspondem a comandos, propriedades e recursos. Se você criar um valor de PROPERTYKEY personalizado, deverá definir uma nova categoria de **GUID** ; Não reutilize os valores de **GUID** WPD ou você correrá o risco de entrar em conflito com o PROPERTYKEYs especificado por WPD existente e futuro.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Visão geral do aplicativo**](application-overview.md)
</dt> <dt>

[**Comandos**](commands.md)
</dt> <dt>

[**GUIDs de formato de objeto**](object-format-guids.md)
</dt> <dt>

[**Propriedades e atributos**](properties-and-attributes.md)
</dt> <dt>

[**Requisitos para objetos**](requirements-for-objects.md)
</dt> </dl>

 

 



