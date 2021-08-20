---
description: Objeto MSDVDAdm
ms.assetid: 753d2820-4d47-4e07-9f54-9b996e55f0b6
title: Objeto MSDVDAdm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa4001def80bff94920996dc627869ffecfd6dda3fbc679be79f2b321ac33a1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072970"
---
# <a name="msdvdadm-object"></a>Objeto MSDVDAdm

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

> [!Note]  
> Essa API está preterida. Para obter informações sobre a reprodução e a navegação de DVD DirectShow, consulte [Aplicativos de DVD](dvd-applications.md).

 

Os métodos e as propriedades do objeto "administração" permitem que um aplicativo de script modifique suas configurações padrão no `MSDVDAdm` Registro ® Windows® Microsoft. O Registro é um banco de dados em todos os Windows em que os aplicativos podem armazenar informações sobre si mesmos para serem usados na inicialização ou durante o tempo de operação.

A maioria desses métodos e propriedades não configura nem recupera os valores atuais no próprio objeto [MSWebDVD.](mswebdvd-object.md) Isso significa, por exemplo, que quando você chama **GetParentalLevel,** o valor retornado não é o nível dos pais atual armazenado no objeto . Em vez disso, é o nível dos pais padrão armazenado no Registro. Para obter o nível dos pais atual, chame o método [**GetPlayerParentalLevel**](getplayerparentallevel-method.md) **MSWebDVD.** Chamar [**SaveParentalLevel**](saveparentallevel-method.md) simplesmente grava um novo nível de acesso dos pais padrão no Registro; você ainda precisa chamar o método **MSWebDVD** [**SelectParentalLevel**](selectparentallevel-method.md) para fazer com que a alteração entre em vigor imediatamente no **objeto MSWebDVD.** Os métodos LCID (identificador de localidade) padrão funcionam de maneira semelhante.

Por outro lado, os métodos [**BookmarkOnStop**](bookmarkonstop-property.md) e [**BookmarkOnClose**](bookmarkonclose-property.md) estão em vigor imediatamente porque o objeto **MSWebDVD** verifica essas configurações antes que o usuário pare a reprodução ou feche o aplicativo, em vez de durante a inicialização.

Você acessa o `MSDVDAdm` objeto por meio da propriedade **DVDAdm** **de MSWebDVD.** Portanto, por exemplo, se o objeto **MSWebDVD** for chamado "DVD", chame **ChangePassword,** conforme mostrado no exemplo de código a seguir.


```C++
DVD.DVDAdm.ChangePassword(sUserName, sOld, sNew)
```



**Métodos e propriedades**

A tabela a seguir lista os métodos e propriedades expostos pelos métodos e propriedades do objeto MSDVDAdm.



| Método                                                          | Descrição                                                                                                                                                                      |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ChangePassword**](changepassword-method.md)                 | Salva uma nova senha de aplicativo no Registro.                                                                                                                                |
| [**SaveParentalLevel**](saveparentallevel-method.md)           | Salva um novo nível dos pais padrão no Registro.                                                                                                                              |
| [**SaveParentalCountry**](saveparentalcountry-method.md)       | Salva o novo país/região dos pais do aplicativo no Registro.                                                                                                             |
| [**Confirmpassword**](confirmpassword-method.md)               | Testa se a senha especificada corresponde à senha salva anteriormente.                                                                                                      |
| [**GetParentalLevel**](getparentallevel-method.md)             | Recupera o nível dos pais que foi salvo pela última vez no Registro.                                                                                                                |
| [**GetParentalCountry**](getparentalcountry-method.md)         | Recupera o país/região dos pais que foi salvo pela última vez no Registro.                                                                                                       |
| [**RestoreScreenSaver**](restorescreensaver-method.md)         | Restaura as configurações de economia de tela do sistema.                                                                                                                                       |
| Propriedade                                                        | Descrição                                                                                                                                                                      |
| [**DisableScreenSaver**](disablescreensaver-property.md)       | Liga ou desliga a economia de tela do sistema.                                                                                                                                         |
| [**DefaultAudioLCID**](defaultaudiolcid-property.md)           | Define ou recupera a configuração do Registro para o LCID padrão especificado pelo usuário para o fluxo de áudio.                                                                                 |
| [**DefaultSubpictureLCID**](defaultsubpicturelcid-property.md) | Define ou recupera a configuração do Registro para o LCID padrão especificado pelo usuário para o fluxo de subpicture.                                                                            |
| [**DefaultMenuLCID**](defaultmenulcid-property.md)             | Define ou recupera a configuração do Registro para o LCID padrão especificado pelo usuário para menus.                                                                                            |
| [**BookmarkOnStop**](bookmarkonstop-property.md)               | Define ou recupera um valor que informa ao objeto MSDVDAdm se é necessário salvar automaticamente um indicador do local atual e as configurações quando o usuário clicar no **botão** Parar. |
| [**BookmarkOnClose**](bookmarkonclose-property.md)             | Define ou recupera um valor que informa ao objeto MSDVDAdm se é necessário salvar automaticamente um indicador do local atual e as configurações quando o usuário fechar o aplicativo.     |



 

 

 



