---
title: Como usar a API de acesso do dispositivo
description: Este tópico contém tarefas e considerações de design para usar a API de acesso do dispositivo.
ms.assetid: 8D951EB5-4AFB-4051-8F1F-30F847F1A757
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: bd1ddf9d2716cd01ab2db8acb08d2793a6831ffa6f20aa2c75378f72932d992b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635296"
---
# <a name="how-to-use-the-device-access-api"></a>Como usar a API de acesso do dispositivo

Este tópico contém tarefas e considerações de design para usar a API de acesso do dispositivo.

## <a name="steps"></a>Etapas

| Tópico | Descrição |
|---|---|
| [Considerações de design para dispositivos personalizados](design.md)<br/> | Este tópico descreve as considerações de design que podem ajudá-lo a determinar se o dispositivo precisa de um driver personalizado.<br/> |
| [Implementar o objeto de acesso do dispositivo](create-the-device-access-object.md)<br/> | Este tópico explica como instanciar o objeto de acesso do dispositivo e usá-lo para acessar um dispositivo. <br/>  |
| [Declarando a capacidade do dispositivo](declaring-the-device-capability.md)<br/> | Este tópico explica como declarar o GUID de capacidade do dispositivo.<br/> |
| [Registrar a interface do dispositivo como restrita a aplicativos com privilégios](register-the-device-interface-class-as-privileged.md)<br/> | Este tópico mostra como adicionar a propriedade **Restricted** que indica que somente aplicativos privilegiados podem acessar uma classe de interface de dispositivo.<br/> |
| [criar uma extensão de Windows Runtime](create-a-windows-runtime-extension.md)<br/> | você pode criar um componente Windows Runtime para encapsular o componente que acessa seu driver. em seguida, você pode escrever um aplicativo de dispositivo de Windows Store para seu dispositivo em C# ou JavaScript.<br/> |

## <a name="additional-resources"></a>Recursos adicionais

- o [exemplo de acesso de Driver personalizado](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample) demonstra como usar as APIs de acesso do dispositivo para acessar um Driver personalizado de um aplicativo de dispositivo do Windows Store.
- os [aplicativos de dispositivo UWP para dispositivos internos](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices) fornecem recursos para aprender mais sobre como projetar e desenvolver Windows aplicativos de dispositivo de armazenamento para dispositivos especializados.
- o [Centro de Desenvolvimento de Hardware](/windows-hardware/drivers/) fornece recursos gerais para as tarefas de desenvolvimento de aplicativo do dispositivo Windows Store que são comuns a todos os tipos de dispositivos.
