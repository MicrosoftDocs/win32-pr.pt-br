---
description: Objeto MSDVDAdm
ms.assetid: 753d2820-4d47-4e07-9f54-9b996e55f0b6
title: Objeto MSDVDAdm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 193d5e46837c576c61b8bf1704ec967c1b6fc246
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087257"
---
# <a name="msdvdadm-object"></a>Objeto MSDVDAdm

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

> [!Note]  
> Essa API está preterida. Para obter informações sobre reprodução e navegação em DVD no DirectShow, consulte [aplicativos de DVD](dvd-applications.md).

 

Os métodos e as propriedades do `MSDVDAdm` objeto "administração" permitem que um aplicativo de script modifique suas configurações padrão no registro do Microsoft® Windows®. O registro é um banco de dados em todos os sistemas Windows, em que os aplicativos podem armazenar informações sobre eles mesmos para serem usados na inicialização ou durante o tempo de execução.

A maioria desses métodos e propriedades não definem ou recuperam os valores atuais no próprio objeto [MSWebDVD](mswebdvd-object.md) . Isso significa, por exemplo, que quando você chama **GetParentalLevel** , o valor retornado não é o nível pai atual armazenado no objeto. Em vez disso, é o nível pai padrão armazenado no registro. Para obter o nível atual do pai, chame o  método MSWebDVD [**GetPlayerParentalLevel**](getplayerparentallevel-method.md). Chamar [**SaveParentalLevel**](saveparentallevel-method.md) simplesmente grava um novo nível de acesso pai padrão no registro; Você ainda precisa chamar o método **MSWebDVD** [**SelectParentalLevel**](selectparentallevel-method.md) para fazer com que a alteração entre em vigor imediatamente no objeto **MSWebDVD** . Os métodos LCID (identificador de localidade) padrão funcionam de maneira semelhante.

Por outro lado, os métodos [**BookmarkOnStop**](bookmarkonstop-property.md) e [**BookmarkOnClose**](bookmarkonclose-property.md) entram em vigor imediatamente porque o objeto **MSWebDVD** verifica essas configurações logo antes de o usuário parar de reproduzir ou fechar o aplicativo, em vez de durante a inicialização.

Você acessa o `MSDVDAdm` objeto por meio da propriedade **DVDAdm** de **MSWebDVD**. Portanto, por exemplo, se o objeto **MSWebDVD** for nomeado "DVD", chame **ChangePassword** , conforme mostrado no exemplo de código a seguir.


```C++
DVD.DVDAdm.ChangePassword(sUserName, sOld, sNew)
```



**Métodos e propriedades**

A tabela a seguir lista os métodos e as propriedades expostas pelos métodos e propriedades do objeto MSDVDAdm.



| Método                                                          | Descrição                                                                                                                                                                      |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ChangePassword**](changepassword-method.md)                 | Salva uma nova senha de aplicativo no registro.                                                                                                                                |
| [**SaveParentalLevel**](saveparentallevel-method.md)           | Salva um novo nível de pai padrão no registro.                                                                                                                              |
| [**SaveParentalCountry**](saveparentalcountry-method.md)       | Salva o novo país/região pai do aplicativo no registro.                                                                                                             |
| [**ConfirmPassword**](confirmpassword-method.md)               | Testa se a senha especificada corresponde à senha salva anteriormente.                                                                                                      |
| [**GetParentalLevel**](getparentallevel-method.md)             | Recupera o nível pai que foi salvo pela última vez no registro.                                                                                                                |
| [**GetParentalCountry**](getparentalcountry-method.md)         | Recupera o país/região pai que foi salvo pela última vez no registro.                                                                                                       |
| [**RestoreScreenSaver**](restorescreensaver-method.md)         | Restaura as configurações de proteção de tela do sistema.                                                                                                                                       |
| Propriedade                                                        | Descrição                                                                                                                                                                      |
| [**DisableScreenSaver**](disablescreensaver-property.md)       | Ativa ou desativa a proteção de tela do sistema.                                                                                                                                         |
| [**DefaultAudioLCID**](defaultaudiolcid-property.md)           | Define ou recupera a configuração do registro para o LCID padrão especificado pelo usuário para o fluxo de áudio.                                                                                 |
| [**DefaultSubpictureLCID**](defaultsubpicturelcid-property.md) | Define ou recupera a configuração do registro para o LCID padrão especificado pelo usuário para o fluxo de subimagem.                                                                            |
| [**DefaultMenuLCID**](defaultmenulcid-property.md)             | Define ou recupera a configuração do registro para o LCID padrão especificado pelo usuário para menus.                                                                                            |
| [**BookmarkOnStop**](bookmarkonstop-property.md)               | Define ou recupera um valor que informa ao objeto MSDVDAdm se é para salvar automaticamente um indicador do local e das configurações atuais quando o usuário clica no botão **parar** . |
| [**BookmarkOnClose**](bookmarkonclose-property.md)             | Define ou recupera um valor que informa ao objeto MSDVDAdm se deve salvar automaticamente um indicador do local e das configurações atuais quando o usuário fechar o aplicativo.     |



 

 

 



