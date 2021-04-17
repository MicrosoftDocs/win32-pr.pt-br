---
description: API do codificador
ms.assetid: 3d19152f-17a3-4576-a2a2-5b827d9ca8d1
title: API do codificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 386b964f44dc4dc69896ead34bbe0d0177b198a1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370277"
---
# <a name="encoder-api"></a>API do codificador

A API do codificador fornece uma interface uniforme para configurar o software e os codificadores de hardware. Os aplicativos podem usar a API do codificador para configurar um codificador e armazenar as definições de configuração. Os fornecedores de codificador podem usar a API do codificador para expor os recursos de um codificador. Embora a API do codificador seja projetada principalmente para codificadores, é geral o suficiente para que os decodificadores também possam dar suporte a ela.

A API do codificador é exposta aos aplicativos por meio da interface [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) , que é exposta pelo filtro do codificador. O filtro do codificador pode ser um filtro do DirectShow nativo, um codificador de hardware ou um DMO (objeto de mídia do DirectX).

-   Filtros de software: um codificador que é implementado como um filtro do DirectShow nativo deve expor o [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) diretamente.
-   Codificadores de hardware: o dispositivo de codificação é exposto por meio de um ou mais AVStream minidrivers, que são representados no modo de usuário pelo KSProxy. KSProxy converte chamadas de método [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) em conjuntos de propriedades KS. Para obter mais informações, consulte a documentação do DDK.
-   DMOs: o DMO deve expor a interface [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) . Os aplicativos do DirectShow podem consultar o filtro de invólucro do DMO, que expõe a interface agregando o DMO. Aplicativos não baseados no DirectShow podem consultar o DMO diretamente.

### <a name="encoder-capabilties"></a>Funcionalidades do codificador

Um codificador pode registrar uma lista de recursos de alto nível armazenando-os no registro do sistema. Cada recurso é identificado por um GUID. Para enumerar os recursos de um codificador específico, faça o seguinte:

1.  Crie o moniker que representa o filtro do codificador. (Consulte [usando o enumerador de dispositivo do sistema](using-the-system-device-enumerator.md).)
2.  Consulte o moniker do filtro para a interface [**IGetCapabilitiesKey**](/windows/desktop/api/Strmif/nn-strmif-igetcapabilitieskey) .
3.  Chame [**IGetCapabilitiesKey:: GetCapabilitiesKey**](/windows/desktop/api/Strmif/nf-strmif-igetcapabilitieskey-getcapabilitieskey). O método retorna um identificador para a chave do registro que contém a lista de recursos do filtro.
4.  Chame a função **RegEnumValue** para enumerar os valores para a chave retornada.

Se você estiver desenvolverndo um codificador, crie as entradas do registro para os recursos quando o filtro for registrado. Para filtros de software, crie uma chave chamada **recursos** que seja adjacente às chaves **FilterData** e **FriendlyName** . Normalmente, você adicionaria essas informações depois de chamar [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) para registrar os dados de filtro padrão. Para obter mais informações, consulte [como registrar filtros do DirectShow](how-to-register-directshow-filters.md). Como alternativa, você pode criar uma chave **CapabilitiesLocation** que contém uma cadeia de caracteres fornecendo a localização da chave de **recursos** no registro. A cadeia de caracteres deve começar com "HKLM \\ ", "HKCR \\ " ou "HKCU \\ " para indicar a subárvore do registro. Para dispositivos Plug and Play, os arquivos de instalação do driver devem criar uma chave de **recursos** adjacente à chave **FriendlyName** do filtro ou usar uma chave **CapabilitiesLocation** , conforme descrito em filtros de software.

Depois de criar a chave de **recursos** , crie um valor para cada GUID de funcionalidade. O nome do valor deve ser a forma de cadeia de caracteres do GUID, no formato `{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}` . Cada tipo de valor deve ser um dos seguintes:

-   Valor numérico único. Use um valor **DWORD** .
-   GUID. Use a forma de cadeia de caracteres do GUID.
-   Pares numéricos. Use uma cadeia de caracteres com o formato "a, b" para representar pares de valores, como largura e altura, ou numerador e denominador para frações.
-   Matrizes de valores. Use várias cadeias de caracteres (**reg \_ sz \_ multi**) para representar mais de um valor.

O exemplo a seguir mostra o layout do registro para um filtro de software:


```C++
\HKCR\CLSID\Filter Category\Instance\Filter CLSID\Capabilities\
    
Values: 
    
    guid1: 1234 (REG_DWORD)   
    
    guid2: "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}" (REG_SZ)
    
    guid3: "2","4","6" (REG_SZ_MULTI)
    
    guid4: "720,480" (REG_SZ) 
```



### <a name="encoder-profiles"></a>Perfis de codificador

Um *perfil de codificador* é uma lista fixa de definições de configuração que podem ser aplicadas a um codificador em tempo de execução. Os perfis são independentes do codificador; um aplicativo pode selecionar um codificador e, em seguida, selecionar um perfil e aplicar as configurações de perfil ao codificador. Os perfis são identificados por GUID e devem ser armazenados no seguinte local no registro:


```C++
\HKLM\Software\Microsoft\EncoderProfiles\Profile GUID\
```



em que *GUID do perfil*

é a forma de cadeia de caracteres do GUID que identifica o perfil. Crie valores para cada configuração. Além disso, crie um valor de cadeia de caracteres chamado "FriendlyName" cujos dados identificam o perfil (como "LowBandwidthVideo").

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Codificador e desenvolvimento de decodificador](encoder-and-decoder-development.md)
</dt> </dl>

 

 



