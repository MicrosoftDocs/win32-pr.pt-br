---
title: Objeto de configurações (SDK do Windows Media Player)
description: O objeto Settings fornece uma maneira de modificar várias configurações do Windows Media Player usando as propriedades e os métodos a seguir.
ms.assetid: f22e8c37-f0c6-4268-a6ed-ce03cff5f3e5
keywords:
- Objeto de configurações Windows Media Player
topic_type:
- apiref
api_name:
- Settings Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d01a521dbccb351045f09dc15d71779fd9362cf4
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/12/2019
ms.locfileid: "103823431"
---
# <a name="settings-object"></a>Objeto de configurações

O objeto **Settings** fornece uma maneira de modificar várias configurações do Windows Media Player usando as propriedades e os métodos a seguir.

O objeto de **configurações** dá suporte às propriedades a seguir.



| Propriedade                                                  | Descrição                                                                                                                      |
|-----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [Inicialização automática](settings-autostart.md)                       | Especifica ou recupera um valor que indica se o item de mídia atual começa a ser reproduzido automaticamente.                           |
| [Lance](settings-balance.md)                           | Especifica ou recupera o saldo de estéreo atual.                                                                               |
| [baseURL](settings-baseurl.md)                           | Especifica ou recupera a URL base usada para resolução de caminho relativo com comandos de script de URL inseridos em arquivos de mídia. |
| [defaultAudioLanguage](settings-defaultaudiolanguage.md) | Recupera o LCID (identificador de localidade) do idioma de áudio padrão especificado no Windows Media Player.                          |
| [DefaultFrame](settings-defaultframe.md)                 | Especifica ou recupera o nome do quadro usado para exibir uma URL recebida em um evento **ScriptCommand** .                |
| [enableErrorDialogs](settings-enableerrordialogs.md)     | Especifica ou recupera um valor que indica se as caixas de diálogo de erro são mostradas automaticamente.                                    |
| [invokeURLs](settings-invokeurls.md)                     | Especifica ou recupera um valor que indica se os eventos de URL devem iniciar um navegador da Web.                                        |
| [isAvailable](settings-isavailable.md)                   | Recupera se um tipo especificado de informação está disponível ou se uma ação especificada pode ser executada.                           |
| [mediaAccessRights](settings-mediaaccessrights.md)       | Recupera um valor que indica os direitos concedidos atualmente para acesso à biblioteca.                                                    |
| [Muta](settings-mute.md)                                 | Especifica ou recupera um valor que indica se o áudio está mudo.                                                                |
| [playCount](settings-playcount.md)                       | Especifica ou recupera o número de vezes que um item de mídia será reproduzido.                                                               |
| [frequência](settings-rate.md)                                 | Especifica ou recupera a taxa de reprodução atual.                                                                                |
| [volume](settings-volume.md)                             | Especifica ou recupera o volume atual.                                                                                       |



 

O objeto de **configurações** dá suporte aos métodos a seguir.



| Método                                                            | Descrição                                                 |
|-------------------------------------------------------------------|-------------------------------------------------------------|
| [GetMode](settings-getmode.md)                                   | Determina se o modo de loop ou de ordem aleatória está ativo. |
| [requestMediaAccessRights](settings-requestmediaaccessrights.md) | Solicita um nível especificado de acesso à biblioteca.        |
| [setmode](settings-setmode.md)                                   | Define o modo de loop ou de ordem aleatória como ativo ou inativo.   |



 

O objeto **Settings** é acessado por meio da propriedade a seguir.



| Objeto                      | Propriedade                        |
|-----------------------------|---------------------------------|
| [Jogador](player-object.md) | [configurações](player-settings.md) |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de modelo de objeto para scripts**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




