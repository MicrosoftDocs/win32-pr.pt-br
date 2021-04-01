---
description: Para os usuários em todo o mundo, a entrada textual faz parte de uma experiência de computação moderna, para Blogs, comentários, tweeting, mensagens instantâneas ou qualquer outro tipo de digitação de texto. No Windows 8, a verificação ortográfica é interna para editar controles.
ms.assetid: ED569D4F-568B-4381-91C3-8EAEDA4DD47C
title: Sobre a API de verificação ortográfica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f0d356823e665781052e2a2d5ea98b358155038
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829017"
---
# <a name="about-the-spell-checking-api"></a>Sobre a API de verificação ortográfica

Para os usuários em todo o mundo, a entrada textual faz parte de uma experiência de computação moderna, para Blogs, comentários, tweeting, mensagens instantâneas ou qualquer outro tipo de digitação de texto. No Windows 8, a verificação ortográfica é interna para editar controles.

Os desenvolvedores podem usar a API de verificação ortográfica em seus aplicativos para consumir os serviços de verificação ortográfica disponíveis. Os desenvolvedores também podem criar verificadores ortográficos que se tornam provedores e são integrados à estrutura de verificação ortográfica do Windows.

A API de verificação ortográfica foi projetada para uso por desenvolvedores Professional C/C++ de aplicativos COM (Windows Component Object Model). Não há suporte para a API de verificação ortográfica para uso em um serviço Windows ou ASP.NET.

## <a name="versioning"></a>Controle de versão

A API de verificação ortográfica está disponível a partir do Windows 8 ou do Windows Server 2012. Adições futuras à API serão tratadas pela criação de novas interfaces que podem ser determinadas usando [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) nos existentes.

## <a name="interfaces"></a>Interfaces

Todas as interfaces devem ser liberadas quando não forem mais usadas. Todas as cadeias de caracteres **LPWSTR** (de saída de parâmetro) retornadas (e itens **LPOLESTR** de [**IEnumString**](/windows/win32/api/objidlbase/nn-objidlbase-ienumstring)) devem ser liberadas com [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) quando não forem mais usadas.

## <a name="error-handling"></a>Tratamento de erros

Os erros são retornados como **HRESULT** s. Não há suporte para [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) e [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) nesta API. Os erros não são particularmente acionáveis, exceto argumentos incorretos.

Os códigos de erro RPC padrão podem ser retornados por qualquer uma das chamadas à API porque estão fora do processo. O tempo limite de RPC padrão é aplicável.

## <a name="security"></a>Segurança

A API de verificação ortográfica pode carregar código externo (provedores de verificação ortográfica). Ele executará esse código fora do processo e sob um contexto de segurança restrito.

## <a name="dictionary-files"></a>Arquivos de dicionário

Os dicionários específicos do usuário para um idioma, que armazenam o conteúdo das listas de palavras que foram adicionadas, excluídas e de AutoCorreção, estão localizados em% AppData% \\ Microsoft \\ Spelling \\ *<language tag>* . Os nomes de FileName são Default. DIC (adicionado), Default. exc (excluído) e default. ACL (AutoCorreção). Os arquivos são texto não criptografado UTF-16 LE que devem começar com a BOM (marca de ordem de byte) apropriada. Cada linha contém uma palavra (nas listas de palavras adicionadas e excluídas) ou um par de AutoCorreção com as palavras separadas por uma barra vertical (" \| ") (na lista de palavras de AutoCorreção). Outros arquivos. dic,. exc e. ACL presentes no diretório serão detectados pelo serviço de verificação ortográfica e adicionados às listas de palavras do usuário. Esses arquivos são considerados somente leitura e não são modificados pela API de verificação ortográfica.

## <a name="installing-a-spell-checking-provider"></a>Instalando um provedor de verificação ortográfica

A instalação de um provedor de verificação ortográfica deve posicionar todos os arquivos que ele usa em um local que permita acesso de leitura do SID ([identificador de segurança](../secauthz/security-identifiers.md)) "todos os pacotes de aplicativos". Instalá-lo em uma pasta em "arquivos de programas" funciona bem. Além disso, o provedor deve definir algumas chaves no registro para que ele apareça para a API de verificação ortográfica. Ele pode estar no hive do \_ usuário atual do hKey \_ ou no \_ hive do computador local hKey \_ , dependendo se ele deve ser instalado somente para o usuário atual ou para todos os usuários.


```
Key: <Registry hive>\SOFTWARE\Classes\CLSID\<Server CLSID>
     Default (REG_SZ) = <Name of the provider>

Key: <Registry hive>\SOFTWARE\Classes\CLSID\<Server CLSID>\InprocServer32
     ThreadingModel (REG_SZ) = "Both"

Key: <Registry hive>\SOFTWARE\Classes\CLSID\<Server CLSID>\Version
     Version (REG_SZ) = <Version>

Key: <Registry hive>\SOFTWARE\Microsoft\Spelling\Spellers\<Provider id string>
     CLSID (REG_SZ) = <CLSID of the COM Server that implements the provider>
```



O [exemplo de provedor de verificação ortográfica](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SpellCheckerProvider) fornece um exemplo do registro necessário para instalar um provedor.

Se você estiver criando novas opções de verificação ortográfica para um provedor de verificação ortográfica, consulte [**IOptionDescription:: ID**](/windows/desktop/api/Spellcheck/nf-spellcheck-ioptiondescription-get_id) para obter orientação sobre nomenclatura.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de API de verificação ortográfica](spell-checker-api-reference.md)
</dt> <dt>

[Exemplo de cliente de verificação ortográfica](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SpellCheckerClient)
</dt> <dt>

[Exemplo de provedor de verificação ortográfica](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SpellCheckerProvider)
</dt> <dt>

[**IOptionDescription:: ID**](/windows/desktop/api/Spellcheck/nf-spellcheck-ioptiondescription-get_id)
</dt> <dt>

[**IEnumString**](/windows/win32/api/objidlbase/nn-objidlbase-ienumstring)
</dt> <dt>

[**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))
</dt> </dl>

 

 
