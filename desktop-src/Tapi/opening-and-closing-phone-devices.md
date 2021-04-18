---
description: Depois de determinar os recursos de um dispositivo de telefone, um aplicativo deve abrir o dispositivo antes que ele possa acessar funções nesse telefone.
ms.assetid: 0215db43-b4d7-4a1e-8d4f-d17013c14e61
title: Abrindo e fechando dispositivos de telefone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4692901d09c680276bda1a5dba77bc57ce599e77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810128"
---
# <a name="opening-and-closing-phone-devices"></a>Abrindo e fechando dispositivos de telefone

Depois de determinar os recursos de um dispositivo de telefone, um aplicativo deve abrir o dispositivo antes que ele possa acessar funções nesse telefone. Depois que um dispositivo de telefone é aberto com êxito, o aplicativo retorna um identificador que representa o telefone aberto. Um dispositivo de telefone pode ser aberto em modos diferentes, fornecendo, assim, uma maneira estruturada de compartilhar um dispositivo de telefone.

A função [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) abre o dispositivo de telefone especificado para conceder ao aplicativo acesso a funções no telefone. Um dispositivo de telefone é identificado como **phoneOpen** por meio de seu identificador de dispositivo, que é passado como o parâmetro *dwDeviceID* .

 

 



