---
description: API do codificador
ms.assetid: 3d19152f-17a3-4576-a2a2-5b827d9ca8d1
title: API do codificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b97dc2242cc718605a851186c726e3301493b7637b94e88b7987868741874a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119823636"
---
# <a name="encoder-api"></a>API do codificador

A API do Codificador fornece uma interface uniforme para configurar codificadores de software e hardware. Os aplicativos podem usar a API do Codificador para configurar um codificador e armazenar as definições de configuração. Os fornecedores do codificador podem usar a API do Codificador para expor os recursos de um codificador. Embora a API do Codificador seja projetada principalmente para codificadores, é geral o suficiente que os decodificadores também possam dar suporte a ela.

A API do Codificador é exposta a aplicativos por meio da interface [**ICodecAPI,**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) que é exposta pelo filtro do codificador. O filtro do codificador pode ser um filtro DirectShow nativo, um codificador de hardware ou um objeto de mídia directX (DMO).

-   Filtros de software: um codificador implementado como um filtro DirectShow nativo deve expor o [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) diretamente.
-   Codificadores de hardware: o dispositivo de codificação é exposto por meio de um ou mais minidrivers AVStream, que são representados no modo de usuário pelo KSProxy. KSProxy converte chamadas de método [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) em conjuntos de propriedades KS. Para obter mais informações, consulte a documentação do DDK.
-   DMOs: o DMO deve expor a interface [**ICodecAPI.**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) DirectShow aplicativos podem consultar o filtro DMO Wrapper, que expõe a interface agregando o DMO. Aplicativos não baseados DirectShow podem consultar o DMO diretamente.

### <a name="encoder-capabilties"></a>Capabilties do codificador

Um codificador pode registrar uma lista de recursos de alto nível, armazenar-os no registro do sistema. Cada funcionalidade é identificada por um GUID. Para enumerar os recursos de um codificador específico, faça o seguinte:

1.  Crie o moniker que representa o filtro do codificador. (Consulte [Usando o enumerador de dispositivo do sistema](using-the-system-device-enumerator.md).)
2.  Consulte o moniker de filtro para a interface [**IGetCapabilitiesKey.**](/windows/desktop/api/Strmif/nn-strmif-igetcapabilitieskey)
3.  Chame [**IGetCapabilitiesKey::GetCapabilitiesKey.**](/windows/desktop/api/Strmif/nf-strmif-igetcapabilitieskey-getcapabilitieskey) O método retorna um handle para a chave do Registro que contém a lista de funcionalidades do filtro.
4.  Chame a **função RegEnumValue** para enumerar os valores da chave retornada.

Se você estiver desvelando um codificador, crie as entradas do Registro para os recursos quando o filtro for registrado. Para filtros de software, crie uma chave chamada **Funcionalidades** adjacente às **chaves FilterData** e **FriendlyName.** Normalmente, você adicionaria essas informações depois de chamar [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) para registrar os dados de filtro padrão. Para obter mais informações, [consulte How to Register DirectShow Filters](how-to-register-directshow-filters.md). Como alternativa, você pode criar uma **chave CapabilitiesLocation** que contém uma cadeia de caracteres que dá o local da **chave Funcionalidades** no Registro. A cadeia de caracteres deve começar com "HKLM", \\ "HKCR" ou \\ "HKCU" para indicar a \\ subárvore do Registro. Para Plug and Play, os arquivos de instalação do driver  devem criar uma chave Funcionalidades adjacente à chave FriendlyName do filtro ou usar uma chave **CapabilitiesLocation,** conforme descrito para filtros de software. 

Depois de criar a **chave Funcionalidades,** crie um valor para cada GUID de funcionalidade. O nome do valor deve ser a forma de cadeia de caracteres do GUID, no formato `{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}` . Cada tipo de valor deve ser um dos seguintes:

-   Valor numérico único. Use um **valor DWORD.**
-   GUID. Use a forma de cadeia de caracteres do GUID.
-   Pares numéricos. Use uma cadeia de caracteres com o formato "a,b" para representar pares de valores, como largura e altura, ou numerador e denominador para frações.
-   Matrizes de valores. Use várias cadeias de caracteres (**REG \_ SZ \_ MULTI**) para representar mais de um valor.

O exemplo a seguir mostra o layout do Registro para um filtro de software:


```C++
\HKCR\CLSID\Filter Category\Instance\Filter CLSID\Capabilities\
    
Values: 
    
    guid1: 1234 (REG_DWORD)   
    
    guid2: "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}" (REG_SZ)
    
    guid3: "2","4","6" (REG_SZ_MULTI)
    
    guid4: "720,480" (REG_SZ) 
```



### <a name="encoder-profiles"></a>Perfis do codificador

Um *perfil de codificador* é uma lista fixa de definições de configuração que podem ser aplicadas a um codificador em tempo de execução. Os perfis são independentes do codificador; um aplicativo pode selecionar um codificador e, em seguida, selecionar um perfil e aplicar as configurações de perfil ao codificador. Os perfis são identificados pelo GUID e devem ser armazenados no seguinte local no Registro:


```C++
\HKLM\Software\Microsoft\EncoderProfiles\Profile GUID\
```



guid *de perfil em que*

é a forma de cadeia de caracteres do GUID que identifica o perfil. Crie valores para cada configuração. Crie também um valor de cadeia de caracteres chamado "FriendlyName" cujos dados identificam o perfil (como "LowBandwidthVideo").

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Desenvolvimento de codificador e decodificador](encoder-and-decoder-development.md)
</dt> </dl>

 

 



