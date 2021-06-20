---
title: Registrando a dependência do aplicativo (Windows Media Player SDK)
description: Saiba como registrar seu aplicativo com componentes de runtime das APIs fornecidas pelo SDK do Windows Media Player.
ms.assetid: 966683d6-e082-448d-8473-baae2311c082
keywords:
- Windows Media Player,configurações do registro de dependência do aplicativo
- Windows Media Player,configurações de registro de dependência
- Windows Media Player,Registro
- registro, configurações de dependência do aplicativo
- registro, configurações de dependência
- registry,settings for Windows Media Player
- configurações do registro de dependência
- configurações do registro de dependência do aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb4b1692c6a4e1a8274472bbe9d718721c1ab4f1
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407359"
---
# <a name="registering-application-dependency-windows-media-player-sdk"></a>Registrando a dependência do aplicativo (Windows Media Player SDK)

Os aplicativos que usam APIs fornecidas pelo SDK do Windows Media Player ou Windows Media Format SDK são dependentes dos componentes de runtime dessas tecnologias. Você pode registrar seu aplicativo como dependente desses componentes como parte da configuração do aplicativo.

Ao registrar seu aplicativo, você pode escolher um dos dois níveis de dependência: bloqueio ou dependente. Quando um ou mais aplicativos são registrados com uma dependência de bloqueio em um dos componentes de runtime, o componente será bloqueado de uma reversões para uma versão anterior. Aplicativos dependentes que não estão registrados como bloqueio não bloqueiam a replicação. Em vez disso, antes que a replicação seja executada, é exibida uma mensagem informando que os aplicativos dependem do componente.

Para registrar seu aplicativo, você deve definir um valor no registro que identifica seu aplicativo. O valor do Registro a ser definido depende do componente do qual seu aplicativo depende. Você também pode definir dois valores adicionais por dependência para fornecer informações adicionais sobre seu aplicativo.

Os seguintes valores de registro são usados para registrar a dependência Windows Media Player runtime do SDK:

-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer \\ Setup REF \\ *\_ TYPE* \\ App, "*APP*", "*APP \_ STRING*"
-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer \\ Setup REF \\ *\_ TYPE* \\ Descritor, "*APP*", "*REF \_ DESCRIPTOR*"
-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer \\ Setup REF \\ *\_ TYPE* \\ Version, "*APP*", "*WMP \_ VERSION*"

Os seguintes valores do Registro são usados para registrar a dependência no runtime Windows Media Format SDK:

-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsMedia Setup REF \\ \\ *\_ TYPE* \\ App, "*APP*", "*APP \_ STRING*"
-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsMedia Setup REF \\ \\ *\_ TYPE* \\ Descritor, "*APP*", "*REF \_ DESCRIPTOR*"
-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsMedia Setup REF \\ \\ *\_ TYPE* \\ Version, "*APP*", "*WMF \_ VERSION*"

As seguintes variáveis são usadas nos valores do Registro listados acima:

*TIPO \_ REF*

Substitua por BlockingRefCounts para bloquear a dependência ou por DependentRefCounts para dependência sem bloqueio.

*APP*

Nome ou descritor curto do seu aplicativo. Essa cadeia de caracteres não será usada em mensagens exibidas para o usuário. Esse valor é o identificador usado em todos os três valores do Registro associados a cada um dos componentes de runtime.

*CADEIA DE CARACTERES DO \_ APLICATIVO*

Descritor do seu aplicativo. Essa cadeia de caracteres pode ser usada em mensagens exibidas para o usuário.

*DESCRITOR \_ REF*

Descrição de como seu aplicativo usa o componente. Esse valor pode incluir um máximo de 256 caracteres.

*VERSÃO DO \_ WMP*

Versão do Windows Media Player exigida pelo seu aplicativo. Se nenhuma versão for especificada, o valor padrão será 9.0.0.0.

*VERSÃO \_ DO WMF*

Versão do Windows Media Format SDK exigido pelo seu aplicativo.

Os três valores de registro de exemplo a seguir demonstram como configurar os valores para seu aplicativo:

-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer \\ Setup \\ DependentRefCounts \\ App, "SouthkeyVideo", "Southkey Video Player"
-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer \\ Setup \\ DependentRefCounts \\ Descriptor, "SouthkeyVideo", "Southkey Video Player uses the Windows Media Format SDK to play video files".
-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer \\ Setup \\ DependentRefCounts \\ Version, "SouthkeyVideo", "9.0.0.2600"

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Configurações do Registro**](registry-settings.md)
</dt> </dl>

 

 




