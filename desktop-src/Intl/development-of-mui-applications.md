---
description: Este tópico resume as principais considerações de programação a ter em mente ao adicionar a funcionalidade de MUI aos seus aplicativos.
ms.assetid: 10064f5c-5563-44f8-afb5-c6c77991e13c
title: Desenvolvimento de aplicativos MUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32cc647069577a2ff3b137573b85308aa66e685df2310c2ea01973d19d1dc0d0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119822766"
---
# <a name="development-of-mui-applications"></a>Desenvolvimento de aplicativos MUI

Este tópico resume as principais considerações de programação a ter em mente ao adicionar a funcionalidade de MUI aos seus aplicativos.

## <a name="requirements-for-a-mui-application"></a>Requisitos para um aplicativo MUI

A funcionalidade de MUI é aplicada somente à localização de um aplicativo totalmente globalizado, criado usando um processo chamado internacionalização de software. O Centro [de DesenvolvedorEs Globais](https://msdn.microsoft.com/goglobal) do Microsoft Go fornece uma ampla seleção de documentação relacionada que ajuda você a projetar, criar e implantar aplicativos prontos para o mundo. Esses documentos ajudam você a considerar como as características de diferentes linguagens humanas podem afetar o design do seu software. Observe que o portal também fornece um arquivo completo das colunas do Dr. International.

Seu aplicativo de MUI pode ser executado em qualquer idioma ou configuração de localidade, e o usuário pode solicitar qualquer idioma para o qual o aplicativo inclua suporte. Portanto, o aplicativo deve codificar o texto da interface do usuário para dar suporte à maior variedade possível de idiomas. O mais importante a ser lembrado é usar [Unicode para](unicode.md) lidar com todo o processamento de texto. Para obter mais informações sobre globalização usando Unicode, consulte o Centro de [DesenvolvedorEs Globais do](https://msdn.microsoft.com/goglobal)Microsoft Go.

## <a name="supported-programming-environments"></a>Ambientes de programação com suporte

Você pode adicionar a funcionalidade de MUI a um aplicativo de formulários Win32 globalizado ou aplicativo de console, conforme descrito neste SDK. Além disso, você pode criar aplicativos gerenciados usando .NET Framework, que é compatível com a MUI. Para obter mais informações, consulte [Desenvolvimento do .NET.](/previous-versions/ff361664(v=vs.100))

## <a name="user-interface-language-settings"></a>Interface do Usuário linguagem Configurações

Ao planejar seu aplicativo de MUI, primeiro você deve decidir sobre os idiomas da interface do usuário e a maneira de apresentá-los ao usuário. O aplicativo pode dar suporte a idiomas de uma destas maneiras:

-   Siga as configurações de idioma do sistema. Suponha que os idiomas de interface do usuário preferenciais do usuário e os idiomas de interface do usuário preferenciais do sistema, juntos, representem os idiomas disponíveis para o usuário. Use o mecanismo de fallback do carregador de recursos para seleção de idioma.
-   Faça configurações de idioma específicas do aplicativo. Dar suporte a idiomas específicos e apresentar um mecanismo de seleção para o usuário.

## <a name="resource-creation"></a>Criação de recursos

Esta seção descreve as possibilidades para criar os recursos de linguagem de interface do usuário para o aplicativo. Para obter mais informações, consulte [Preparando recursos](preparing-resources.md).

> [!Note]  
> Em sistemas operacionais Windows Vista pré-Windows, você geralmente cria aplicativos localizados de idioma único estáticos e empacotados separadamente com os idiomas com suporte nas seções de recursos incluídas nos arquivos executáveis. Esse tipo de implementação é amplamente obsoleto e é recomendável escolher uma das outras técnicas de criação de recursos descritas nesta seção, com suporte para Windows Vista e posterior. O aplicativo pode ser feito para ser executado em sistemas operacionais Windows Vista previamente com o uso de [**LoadMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya).

 

### <a name="use-of-a-single-language-in-a-resource-dll-mui-resource-technology"></a>Uso de uma única linguagem em uma DLL de recurso (tecnologia de recursos da MUI)

Uma implementação de recurso de DLL satélite padrão é usada por muitos aplicativos da Microsoft. Nesse caso, um arquivo executável principal é usado para o aplicativo MUI e uma DLL de recurso é criada para cada idioma com suporte. O uso de uma DLL satélite se aplica a aplicativos executados em qualquer Windows operacional. Conforme descrito em [Gerenciamento de Recursos da MUI,](mui-resource-management.md)a tecnologia de recursos da MUI dá suporte a uma variação na implementação de DLL satélite padrão.

### <a name="use-of-multiple-languages-in-a-resource-dll"></a>Uso de vários idiomas em uma DLL de recurso

Você pode optar por criar um arquivo executável principal para seu aplicativo MUI e uma DLL de recurso para os recursos associados aos idiomas com suporte. Cópias do mesmo identificador de recurso são definidas no arquivo de recurso de linguagem base (extensão .rc) em marcas de idioma diferentes para todos os idiomas com suporte.

### <a name="use-of-an-application-specific-resource-mechanism"></a>Uso de um mecanismo Application-Specific recursos

Você pode planejar seu aplicativo MUI para usar um mecanismo de recurso personalizado. Nesse caso, o aplicativo lida com o carregamento de recursos de maneira especializada.

## <a name="resource-localization"></a>Localização de recursos

Para dar suporte às linguagens de interface do usuário para seu aplicativo MUI, você deve ter os recursos de linguagem localizados. A MUI dá suporte a dois tipos de localização, conforme descrito na tabela a seguir.



| Tipo de localização       | Descrição                                                                                                                                                                                                                                                                |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Localização de pré-build  | Solicite a localização antes de criar o aplicativo e os recursos específicos do idioma. O arquivo de recurso de linguagem base para as linguagens de interface do usuário com suporte é copiado e renomeado para cada idioma com suporte, e as cópias são fornecidas aos localizadores conforme necessário. |
| Localização pós-build | Solicite a localização depois de criar o arquivo executável e a DLL de recurso para seu aplicativo. Nesse caso, uma cópia da DLL de recurso é fornecida para cada localizador.                                                                                                     |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre Interface de Usuário Multilíngue](about-multilingual-user-interface.md)
</dt> </dl>

 

 
