---
description: A tabela MIME associa um tipo de conteúdo MIME com uma extensão de nome de arquivo ou um CLSID para gerar a extensão ou as informações do servidor COM necessárias para o anúncio do conteúdo MIME (Multipurpose Internet Mail Extensions).
ms.assetid: 5d452b24-ae04-4c45-8b3b-48e81f13a21e
title: Tabela MIME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca11c8596e8f3735872c88668211953fc2b18b52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170834"
---
# <a name="mime-table"></a>Tabela MIME

A tabela MIME associa um tipo de conteúdo MIME com uma extensão de nome de arquivo ou um CLSID para gerar a extensão ou as informações do servidor COM necessárias para o anúncio do conteúdo MIME (Multipurpose Internet Mail Extensions).

A tabela MIME tem as colunas a seguir.



| Coluna      | Tipo             | Chave | Nullable |
|-------------|------------------|-----|----------|
| ContentType | [Text](text.md) | S   | N        |
| Extensão\_ | [Text](text.md) | N   | N        |
| CLSID       | [GUID](guid.md) | N   | S        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="ContentType"></span><span id="contenttype"></span><span id="CONTENTTYPE"></span>ContentType
</dt> <dd>

Esta coluna é um identificador para o conteúdo MIME. Normalmente, ele é escrito na forma de tipo/formato.

</dd> <dt>

<span id="Extension_"></span><span id="extension_"></span><span id="EXTENSION_"></span>Extensão\_
</dt> <dd>

Esta coluna contém a extensão de servidor que deve ser associada ao conteúdo MIME, sem o ponto. Esta coluna é uma chave estrangeira na [tabela de extensão](extension-table.md). A tabela de extensão contém informações de servidor de extensão de nome de arquivo que são usadas como parte do anúncio.

</dd> <dt>

<span id="CLSID"></span><span id="clsid"></span>CLSID
</dt> <dd>

Esta coluna contém o CLSID do servidor COM que deve ser associado ao conteúdo MIME. O CLSID nesta coluna pode ser uma chave estrangeira na tabela de [classes](class-table.md) ou pode ser um CLSID que já existe na máquina do usuário. A tabela de classes contém informações relacionadas ao servidor COM que são usadas como parte do anúncio.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa tabela é referida quando a ação [RegisterMIMEInfo](registermimeinfo-action.md) ou a [ação UnregisterMIMEInfo](unregistermimeinfo-action.md) é executada. No modo de anúncio, a ação RegisterMIMEInfo registra todas as informações de MIME para servidores da tabela MIME para a qual o recurso correspondente está habilitado. Caso contrário, a ação registrará informações de MIME para servidores da tabela MIME para as quais o recurso correspondente está selecionado no momento para ser instalado. A [ação UnregisterMIMEInfo](unregistermimeinfo-action.md) cancela o registro das informações do registro relacionadas a MIME do sistema. A ação cancela o registro de informações de MIME para servidores da tabela MIME para a qual o recurso correspondente está selecionado no momento para ser desinstalado.

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE15](ice15.md)  
[ICE32](ice32.md)  
</dl>

 

 



