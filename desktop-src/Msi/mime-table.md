---
description: A tabela MIME associa um tipo de conteúdo MIME a uma extensão de nome de arquivo ou CLSID para gerar a extensão ou as informações do servidor COM necessárias para o anúncio do conteúdo mime (Extensões multipropósico do Internet Mail).
ms.assetid: 5d452b24-ae04-4c45-8b3b-48e81f13a21e
title: Tabela MIME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9e8a8f83499e286b63bf24dffa8858329231e74eec1f641588230da51578007
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913366"
---
# <a name="mime-table"></a>Tabela MIME

A tabela MIME associa um tipo de conteúdo MIME a uma extensão de nome de arquivo ou CLSID para gerar a extensão ou as informações do servidor COM necessárias para o anúncio do conteúdo mime (Extensões multipropósico do Internet Mail).

A tabela MIME tem as seguintes colunas.



| Coluna      | Tipo             | Chave | Nullable |
|-------------|------------------|-----|----------|
| ContentType | [Text](text.md) | Y   | N        |
| Extensão\_ | [Text](text.md) | N   | N        |
| CLSID       | [GUID](guid.md) | N   | Y        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="ContentType"></span><span id="contenttype"></span><span id="CONTENTTYPE"></span>Contenttype
</dt> <dd>

Essa coluna é um identificador para o conteúdo mime. Normalmente, ele é escrito na forma de tipo/formato.

</dd> <dt>

<span id="Extension_"></span><span id="extension_"></span><span id="EXTENSION_"></span>Extensão\_
</dt> <dd>

Essa coluna contém a extensão de servidor que deve ser associada ao conteúdo MIME, sem o ponto. Essa coluna é uma chave estrangeira na tabela [Extensão](extension-table.md). A tabela Extensão contém informações do servidor de extensão de nome de arquivo que são usadas como parte do anúncio.

</dd> <dt>

<span id="CLSID"></span><span id="clsid"></span>Clsid
</dt> <dd>

Essa coluna contém a CLSID do servidor COM que deve ser associada ao conteúdo mime. O CLSID nessa coluna pode ser uma chave estrangeira na tabela [Classe](class-table.md) ou pode ser um CLSID que já existe no computador do usuário. A tabela Classe contém informações relacionadas ao servidor COM que são usadas como parte do anúncio.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa tabela é referenciada quando [a ação RegisterMIMEInfo](registermimeinfo-action.md) ou [a ação UnregisterMIMEInfo](unregistermimeinfo-action.md) é executada. No modo de anúncio, a ação RegisterMIMEInfo registra todas as informações mime para servidores da tabela MIME para a qual o recurso correspondente está habilitado. Caso contrário, a ação registrará informações mime para servidores da tabela MIME para a qual o recurso correspondente está selecionado para ser instalado no momento. A [ação UnregisterMIMEInfo](unregistermimeinfo-action.md) não registra informações de registro relacionadas ao MIME do sistema. A ação desinstala as informações do MIME para servidores da tabela MIME para a qual o recurso correspondente está selecionado para ser desinstalado.

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE15](ice15.md)  
[ICE32](ice32.md)  
</dl>

 

 



