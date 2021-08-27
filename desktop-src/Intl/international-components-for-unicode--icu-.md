---
description: O ICU (componentes internacionais para Unicode) é um conjunto maduro e amplamente utilizado de APIs de globalização de código aberto.
ms.assetid: 4AEBE391-4121-44B2-B15B-0032645D7053
title: ICU (Componentes Internacionais para Unicode)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c7fec661b24e352c24abddf687e6b119752e39ce80c12dc409000afa179f1f7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107016"
---
# <a name="international-components-for-unicode-icu"></a>ICU (Componentes Internacionais para Unicode)

O ICU (componentes internacionais para Unicode) é um conjunto maduro e amplamente utilizado de APIs de globalização de código aberto. O ICU utiliza o CLDR (repositório de dados de localidade comum) de Unicode como sua biblioteca de dados, fornecendo suporte à globalização para aplicativos de software. O ICU é amplamente portátil e dá aos aplicativos os mesmos resultados em todas as plataformas.

## <a name="highlights-of-the-globalization-api-services-provided-by-icu"></a>Destaques dos serviços de API de globalização fornecidos pelo ICU

-   **Conversão de página de código**: converter dados de texto de ou para Unicode e praticamente qualquer outro conjunto de caracteres ou codificação. As tabelas de conversão do ICU são baseadas nos dados de conjunto de caracteres coletados pela IBM ao longo de muitas décadas, e é a mais completa disponível em qualquer lugar.
-   **Agrupamento**: comparar cadeias de caracteres de acordo com as convenções e os padrões de um idioma, região ou país específico. O agrupamento do ICU é baseado no algoritmo de agrupamento Unicode mais regras de comparação específicas de localidade do CLDR.
-   **Formatação**: formatar números, datas, horas e valores de moeda de acordo com as convenções de uma localidade escolhida. Isso inclui a tradução de nomes de mês e dia para o idioma selecionado, a escolha de abreviaturas apropriadas, a ordenação de campos corretamente, etc. Esses dados também vêm do repositório de dados de localidade comum.
-   **Cálculos de tempo**: vários tipos de calendários são fornecidos além do gregoriano tradicional. Um conjunto completo de APIs de cálculo de fuso horário é fornecido.
-   **Suporte a Unicode**: o ICU rastreia com precisão o padrão Unicode, fornecendo acesso fácil a todas as muitas propriedades de caractere Unicode, normalização Unicode, dobramento de caso e outras operações fundamentais, conforme especificado pelo [padrão Unicode](https://www.unicode.org/).
-   **Expressão regular**: as expressões regulares do ICU oferecem suporte total ao Unicode e, ao mesmo tempo, fornecem um desempenho muito competitivo.
-   **Bidi**: suporte para tratamento de texto que contém uma mistura de dados da esquerda para a direita (inglês) e da direita para a esquerda (árabe ou Hebraico).

Para obter mais informações, você pode visitar o site do ICU: <http://site.icu-project.org/>

## <a name="overview"></a>Visão geral

no Atualização do Windows 10 para Criadores, o ICU foi integrado ao Windows, tornando as APIs e os dados do C acessíveis publicamente.

> [!IMPORTANT]
> a versão do ICU no Windows expõe apenas as APIs C. Ele não expõe nenhuma das APIs do C++. Infelizmente, é impossível expor as APIs do C++ devido à falta de uma ABI estável em C++.

Para obter a documentação sobre as APIs do ICU C, consulte a página de documentação oficial do ICU aqui: <http://icu-project.org/apiref/icu4c/index.html#Module>

## <a name="history-of-changes-to-the-icu-library-in-windows"></a>Histórico de alterações na biblioteca do ICU no Windows

### <a name="version-1703-creators-update"></a>Versão 1703 (atualização para criadores)
A biblioteca ICU foi adicionada primeiro ao sistema operacional Windows 10 nesta versão.
Ele foi adicionado como:
- Duas DLLs do sistema:
    -   **icuuc.dll** (esta é a biblioteca "comum" do ICU)
    -   **icuin.dll** (esta é a biblioteca de "i18n" do ICU)
- dois arquivos de cabeçalho no SDK do Windows 10:
    -   **icucommon. h**
    -   **icui18n. h**
- dois bibliotecas de importação no SDK do Windows 10:
    -   **icuuc. lib**
    -   **icuin. lib**

### <a name="version-1709-fall-creators-update"></a>Versão 1709 (atualização para criadores de outono)
Um arquivo de cabeçalho combinado, **ICU. h**, foi adicionado, que contém o conteúdo de ambos os arquivos de cabeçalho acima (icucommon. h e icui18n. h) e também altera o tipo de `UCHAR` para `char16_t` .

### <a name="version-1903-may-2019-update"></a>Versão 1903 (atualização de maio de 2019)
Uma nova DLL combinada, **icu.dll**, foi adicionada, que contém as bibliotecas "comum" e "i18n". além disso, uma nova biblioteca de importação foi adicionada ao SDK do Windows 10: **icu. lib**.

No futuro, nenhuma nova API será adicionada aos cabeçalhos antigos (icucommon. h e icui18n. h) ou ao bibliotecas de importação antigo (icuuc. lib e icuin. lib). Novas APIs serão adicionadas somente ao cabeçalho combinado (ICU. h) e à lib de importação combinada (ICU. lib).

## <a name="getting-started"></a>Introdução

há três etapas principais a seguir: (Atualização do Windows 10 para Criadores ou superior)

<dl>

1. seu aplicativo precisa direcionar Windows 10 versão 1703 (atualização para criadores) ou superior.

2. Adicionar nos cabeçalhos:

   ``` syntax
   #include <icucommon.h>
   #include <icui18n.h>
   ```

   no Windows 10 versão 1709 e superior, você deve incluir o cabeçalho combinado:

   ``` syntax
   #include <icu.h>
   ```
  
3. Link para as duas bibliotecas:

   -   icuuc. lib
   -   icuin. lib

   no Windows 10 versão 1903 e superior, você deve usar a biblioteca combinada:

   -   ICU. lib

</dl>

Em seguida, você pode chamar qualquer API do ICU C dessas bibliotecas que desejar. (Nenhuma API C++ é exposta.)

> [!IMPORTANT]
> Se você estiver usando as bibliotecas de importação herdadas, icuuc. lib e icuin. lib, verifique se elas estão listadas antes das bibliotecas de abrangência, como onecoreuap. lib ou WindowsApp. lib, na configuração do vinculador de dependências adicionais (consulte a imagem abaixo). Caso contrário, o vinculador será vinculado a ICU. lib, o que resultará em uma tentativa de carregar icu.dll durante o tempo de execução. Essa DLL está presente apenas começando com a versão 1903. portanto, se um usuário atualizar o SDK do Windows 10 em uma máquina Windows anterior à versão 1903, o aplicativo não será carregado e executado. para obter um histórico das bibliotecas icu no Windows, consulte [histórico de alterações na biblioteca do icu em Windows](#history-of-changes-to-the-icu-library-in-windows).

![exemplo de ICU](images/icu-example.png)

> [!Note]  
>
> - Esta é a configuração para "todas as plataformas".
> - Para que os aplicativos Win32 usem o ICU, eles precisam chamar [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) primeiro. no Windows 10 versão 1903 e superior, em que a biblioteca ICU combinada (icu.dll/icu.lib) está disponível, você pode omitir a chamada CoInitializeEx usando a biblioteca combinada.
> - nem todos os dados retornados por APIs ICU serão alinhados com o sistema operacional Windows, pois esse trabalho de alinhamento ainda está em andamento. 

## <a name="icu-example-app"></a>Aplicativo de exemplo do ICU

### <a name="example-code-snippet"></a>Trecho de código de exemplo

Veja a seguir um exemplo que ilustra o uso de APIs do ICU de dentro de um aplicativo UWP do C++. (Não se destina a ser um aplicativo autônomo completo, em vez disso, é apenas um exemplo de chamada de um método ICU.)

O exemplo pequeno a seguir pressupõe que há métodos **ErrorMessage** e **OutputMessage** que geram as cadeias de caracteres para o usuário de alguma maneira.

``` syntax
// On Windows 10 Creators Update, include the following two headers. With Windows 10 Fall Creators Update and later, you can just include the single header <icu.h>.
#include <icucommon.h>
#include <icui18n.h>

void FormatDateTimeICU()
{
    UErrorCode status = U_ZERO_ERROR;

    // Create a ICU date formatter, using only the 'short date' style format.
    UDateFormat* dateFormatter = udat_open(UDAT_NONE, UDAT_SHORT, nullptr, nullptr, -1, nullptr, 0, &status);

    if (U_FAILURE(status))
    {
        ErrorMessage(L"Failed to create date formatter.");
        return;
    }

    // Get the current date and time.
    UDate currentDateTime = ucal_getNow();

    int32_t stringSize = 0;
    
    // Determine how large the formatted string from ICU would be.
    stringSize = udat_format(dateFormatter, currentDateTime, nullptr, 0, nullptr, &status);

    if (status == U_BUFFER_OVERFLOW_ERROR)
    {
        status = U_ZERO_ERROR;
        // Allocate space for the formatted string.
        auto dateString = std::make_unique<UChar[]>(stringSize + 1);

        // Format the date time into the string.
        udat_format(dateFormatter, currentDateTime, dateString.get(), stringSize + 1, nullptr, &status);

        if (U_FAILURE(status))
        {
            ErrorMessage(L"Failed to format the date time.");
            return;
        }

        // Output the formatted date time.
        OutputMessage(dateString.get());
    }
    else
    {
        ErrorMessage(L"An error occured while trying to determine the size of the formatted date time.");
        return;
    }

    // We need to close the ICU date formatter.
    udat_close(dateFormatter);
}
```

 

 



