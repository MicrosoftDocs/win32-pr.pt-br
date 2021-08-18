---
description: Depois de determinar os recursos de um dispositivo de telefone, um aplicativo deve abrir o dispositivo antes de poder acessar funções nesse telefone.
ms.assetid: 0215db43-b4d7-4a1e-8d4f-d17013c14e61
title: Abrindo e fechando Telefone dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6dacda3e98e96ed4a11334443a7b99b949e6d1b3823e42e1790c5a346b52dac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012512"
---
# <a name="opening-and-closing-phone-devices"></a>Abrindo e fechando Telefone dispositivos

Depois de determinar os recursos de um dispositivo de telefone, um aplicativo deve abrir o dispositivo antes de poder acessar funções nesse telefone. Depois que um dispositivo de telefone tiver sido aberto com êxito, o aplicativo retornará uma alça que representa o telefone aberto. Um dispositivo de telefone pode ser aberto em modos diferentes, fornecendo assim uma maneira estruturada de compartilhar um dispositivo de telefone.

A [**função phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) abre o dispositivo de telefone especificado para dar ao aplicativo acesso às funções no telefone. Um dispositivo de telefone é identificado como **phoneOpen** por meio de seu identificador de dispositivo, que é passado como o *parâmetro dwDeviceID.*

 

 



