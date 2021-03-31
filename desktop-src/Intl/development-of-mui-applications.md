---
description: Este tópico resume as principais considerações de programação para ter em mente ao adicionar a funcionalidade do MUI aos seus aplicativos.
ms.assetid: 10064f5c-5563-44f8-afb5-c6c77991e13c
title: Desenvolvimento de aplicativos MUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb4a3278b4cc70969c1aa968de895d99fd3363a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829796"
---
# <a name="development-of-mui-applications"></a>Desenvolvimento de aplicativos MUI

Este tópico resume as principais considerações de programação para ter em mente ao adicionar a funcionalidade do MUI aos seus aplicativos.

## <a name="requirements-for-a-mui-application"></a>Requisitos para um aplicativo MUI

A funcionalidade do MUI é aplicada somente à localização de um aplicativo totalmente globalizado, criada usando um processo chamado internacionalização de software. O Microsoft [Go Global Developer Center](https://msdn.microsoft.com/goglobal) fornece uma ampla seleção de documentação relacionada que ajuda você a projetar, criar e implantar aplicativos preparados para o mundo. Esses documentos ajudam você a considerar como as características de diferentes idiomas humanos podem afetar o design do seu software. Observe que o portal também fornece um arquivo completo de colunas Dr. International.

Seu aplicativo MUI pode ser executado sob qualquer idioma ou configuração de localidade, e o usuário pode solicitar qualquer idioma para o qual o aplicativo inclui suporte. Portanto, o aplicativo deve codificar o texto da interface do usuário para dar suporte à maior variedade possível de linguagens. A coisa mais importante a ser lembrada é usar o [Unicode](unicode.md) para lidar com todo o processamento de texto. Para obter mais informações sobre a globalização usando Unicode, consulte o centro de desenvolvedores do Microsoft [Go Global](https://msdn.microsoft.com/goglobal).

## <a name="supported-programming-environments"></a>Ambientes de programação com suporte

Você pode adicionar a funcionalidade do MUI a um aplicativo de console, ou aplicativo de formulários Win32 globalizado, conforme descrito neste SDK. Além disso, você pode criar aplicativos gerenciados usando o .NET Framework, que é compatível com o MUI. Para obter mais informações, consulte [.NET Development](/previous-versions/ff361664(v=vs.100)).

## <a name="user-interface-language-settings"></a>Configurações de idioma da interface do usuário

Ao planejar seu aplicativo MUI, primeiro você deve decidir sobre os idiomas da interface do usuário e a maneira de apresentá-los ao usuário. O aplicativo pode dar suporte a idiomas de uma destas maneiras:

-   Siga as configurações de idioma do sistema. Suponha que as linguagens de interface do usuário preferenciais e os idiomas de interface de usuário preferenciais do sistema, reunidos, representem os idiomas disponíveis para o usuário. Use o mecanismo de fallback do carregador de recursos para seleção de idioma.
-   Faça configurações de idioma específicas do aplicativo. Dar suporte a idiomas específicos e apresentar um mecanismo de seleção para o usuário.

## <a name="resource-creation"></a>Criação de recursos

Esta seção descreve as possibilidades para criar os recursos de idioma da interface do usuário para o aplicativo. Para obter mais informações, consulte [preparando recursos](preparing-resources.md).

> [!Note]  
> Em sistemas operacionais anteriores ao Windows Vista, você geralmente cria aplicativos de um único idioma com pacote estático e separadamente com os idiomas com suporte nas seções de recursos incluídas nos arquivos executáveis. Esse tipo de implementação é amplamente obsoleto e é recomendável escolher uma das outras técnicas de criação de recursos descritas nesta seção, com suporte para o Windows Vista e posterior. O aplicativo pode ser feito para ser executado em sistemas operacionais anteriores ao Windows Vista pelo uso de [**LoadMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya).

 

### <a name="use-of-a-single-language-in-a-resource-dll-mui-resource-technology"></a>Uso de um único idioma em uma DLL de recurso (tecnologia de recursos do MUI)

Uma implementação de recurso de DLL satélite padrão é usada por muitos aplicativos da Microsoft. Nesse caso, um arquivo executável principal é usado para o aplicativo MUI e uma DLL de recurso é criada para cada idioma com suporte. O uso de uma DLL satélite se aplica a aplicativos executados em qualquer sistema operacional Windows. Conforme descrito em [Gerenciamento de recursos do MUI](mui-resource-management.md), a tecnologia de recursos do MUI dá suporte a uma variação na implementação da DLL satélite padrão.

### <a name="use-of-multiple-languages-in-a-resource-dll"></a>Uso de vários idiomas em uma DLL de recurso

Você pode optar por criar um arquivo executável principal para seu aplicativo MUI e uma DLL de recurso para os recursos associados a idiomas com suporte. Cópias do mesmo identificador de recurso são definidas no arquivo de recurso de idioma base (extensão. rc) em marcas de idioma diferentes para todos os idiomas com suporte.

### <a name="use-of-an-application-specific-resource-mechanism"></a>Uso de um mecanismo de recurso Application-Specific

Você pode planejar seu aplicativo MUI para usar um mecanismo de recurso personalizado. Nesse caso, o aplicativo manipula seu carregamento de recursos de forma especializada.

## <a name="resource-localization"></a>Localização de recursos

Para dar suporte aos idiomas da interface do usuário para seu aplicativo MUI, você deve ter os recursos de idioma localizados. O MUI dá suporte a dois tipos de localização, conforme descrito na tabela a seguir.



| Tipo de localização       | Descrição                                                                                                                                                                                                                                                                |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Localização de pré-compilação  | Solicite a localização antes de compilar os recursos específicos do aplicativo e do idioma. O arquivo de recurso de idioma base para os idiomas da interface do usuário com suporte é copiado e renomeado para cada idioma com suporte, e as cópias são fornecidas aos localizadores, conforme necessário. |
| Localização pós-compilação | Solicite a localização depois de criar o arquivo executável e a DLL de recursos para seu aplicativo. Nesse caso, uma cópia da DLL de recurso é fornecida para cada localizador.                                                                                                     |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre a interface do usuário multilíngue](about-multilingual-user-interface.md)
</dt> </dl>

 

 
