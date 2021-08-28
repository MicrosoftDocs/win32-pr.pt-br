---
title: Obtendo um SDO de máquina
description: A primeira etapa ao usar a API de SDO é criar um objeto de computador SDO.
ms.assetid: bdb01437-08d0-4279-94f2-840cb786cc44
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9217333440235d5adac544e00420f8564513510908a89a1da7494cf7ba2772ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128596"
---
# <a name="obtaining-a-machine-sdo"></a>Obtendo um SDO de máquina

A primeira etapa ao usar a API de SDO é criar um objeto de computador SDO.

Use a função [**CLSIDFromProgID**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid) para obter o identificador de classe (CLSID) para o objeto de computador SDO. O identificador programático (ProgID) a ser usado para o objeto é "IAS. SdoMachine".

Quando você tiver o CLSID, chame [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) com esse CLSID. Especifique [**ISdoMachine**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine) como a interface para a qual retornar um ponteiro.

Consulte [anexando a um computador SDO-Enabled](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer) para ver o código de exemplo que demonstra como obter um SDO de máquina.

 

 