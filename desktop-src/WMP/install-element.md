---
title: Elemento de instalação
description: Observação Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online. O elemento install especifica os valores usados pelo Windows Media Player para instalar uma loja online.
ms.assetid: 9a5e15ee-ec36-48d3-a1c2-bf20b6d2da48
keywords:
- Instalar o elemento Windows Media Player
topic_type:
- apiref
api_name:
- Install Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bba56240651f789b45c18b006b16e5e07b10676e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760255"
---
# <a name="install-element"></a>Elemento de instalação

> [!Note]  
> Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

O elemento **install** especifica os valores usados pelo Windows Media Player para instalar uma loja online.

``` syntax
<Install
    EULAURL = "URL"
    CodeURL = "URL"
    PrivacyInfoURL = "URL"
    InstallApp = "filename"
    InstallData = "commandline"
    CatalogURL = "URL"
/>
```

## <a name="attributes"></a>Atributos

<dl> <dt>

<span id="EULAURL__required_"></span><span id="eulaurl__required_"></span><span id="EULAURL__REQUIRED_"></span>**EULAURL** (obrigatório)
</dt> <dd>

URL totalmente qualificada para um arquivo com uma extensão de nome de arquivo. txt que o Windows Media Player usa para exibir um EULA (contrato de licença de usuário final). Esse arquivo deve ser codificado no formato ANSI.

</dd> <dt>

<span id="CodeURL__required_"></span><span id="codeurl__required_"></span><span id="CODEURL__REQUIRED_"></span>**CodeURL** (obrigatório)
</dt> <dd>

URL totalmente qualificada para um pacote, com uma extensão de nome de arquivo. cab, que é usada para instalar a loja online. O pacote e todos os módulos de código no pacote devem ser assinados. Para obter informações sobre assinatura de código, consulte [introdução à assinatura de código](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)) na biblioteca MSDN.

</dd> <dt>

<span id="PrivacyInfoURL__required_"></span><span id="privacyinfourl__required_"></span><span id="PRIVACYINFOURL__REQUIRED_"></span>**PrivacyInfoURL** (obrigatório)
</dt> <dd>

URL totalmente qualificada para uma página da Web que contém informações de política de privacidade para a loja online.

</dd> <dt>

<span id="InstallApp__required_"></span><span id="installapp__required_"></span><span id="INSTALLAPP__REQUIRED_"></span>**InstallApp** (obrigatório)
</dt> <dd>

Nome do arquivo EXE ou INF a ser executado. Esse arquivo deve estar contido no arquivo CAB especificado pelo atributo **CodeURL** .

</dd> <dt>

<span id="InstallData__optional_"></span><span id="installdata__optional_"></span><span id="INSTALLDATA__OPTIONAL_"></span>**InstallData** (opcional)
</dt> <dd>

Cadeia de caracteres de linha de comando que é passada para o aplicativo especificado pelo atributo **InstallApp** . Esse atributo só é aplicável quando o valor de **InstallApp** especifica um executável.

</dd> <dt>

<span id="CatalogURL__required_for_type_1__ignored_for_type_2_"></span><span id="catalogurl__required_for_type_1__ignored_for_type_2_"></span><span id="CATALOGURL__REQUIRED_FOR_TYPE_1__IGNORED_FOR_TYPE_2_"></span>**CatalogURL** (necessário para o tipo 1, ignorado para o tipo 2)
</dt> <dd>

URL totalmente qualificada para o catálogo compilado do repositório online.

</dd> </dl>

## <a name="parentchild-elements"></a>Elementos pai/filho



| Hierarquia       | Elemento         |
|-----------------|-----------------|
| Elementos pai | **ServiceInfo** |
| Elementos filho  | Nenhum            |



 

## <a name="remarks"></a>Comentários

Se algum dos atributos necessários estiver ausente ou não estiver disponível, a instalação do Windows Media Player não tentará baixar e instalar o código do provedor de loja online. A instalação configurará os valores padrão offline, conforme especificado no documento do **serviceInfo** . O **serviceInfo** pode ser usado quando não estiver conectado à Internet, passando o nome do provedor padrão e as informações do **serviceInfo** como parâmetros de linha de comando. Consulte [redistribuindo o software do Windows Media Player](redistributing-windows-media-player-software.md) para obter detalhes sobre as opções de linha de comando.

> [!Note]  
> O uso deste elemento requer que você assine um contrato de redistribuição com a Microsoft. Entre em contato com seu representante de negócios para obter detalhes.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------|
| Versão<br/> | Windows Media Player 10 ou posterior.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Documento de informações de exemplo para uma loja online tipo 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Documento de informações de exemplo para uma loja online tipo 2**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Documento do serviceInfo**](serviceinfo-document.md)
</dt> </dl>

 

