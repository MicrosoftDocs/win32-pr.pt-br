---
title: Glossário do sistema de arquivos projetado do Windows
description: Termos especiais usados em ProjFS.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: c6eac8faa83e2c898e4b1a3ada5c24ef81151b22
ms.sourcegitcommit: a48b68a75323edfb902eb04fbe6d0ecba6988c21
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/21/2020
ms.locfileid: "105773924"
---
# <a name="windows-projected-file-system-glossary"></a>Glossário do sistema de arquivos projetado do Windows

Termos especiais usados em ProjFS.

<dl>
<dt>

<span id="projfs.glossary_backing_store"></span><span id="PROJFS.GLOSSARY_BACKING_STORE"></span>**repositório de backup**
</dt>
<dd>

Dados hierárquicos mantidos pelo provedor que são projetados no sistema de arquivos como arquivos e diretórios.
</dd>

<dt>

<span id="projfs.glossary_dirty_placeholder"></span><span id="PROJFS.GLOSSARY_DIRTY_PLACEHOLDER"></span>**espaço reservado sujo**
</dt>
<dd>

Um arquivo ou diretório que foi modificado localmente e não é mais um cache de seu estado no repositório do provedor.  Consulte [estado do cache na raiz de virtualização](cache-state.md).
</dd>

<dt>

<span id="projfs.glossary_full_file_directory"></span><span id="PROJFS.GLOSSARY_FULL_FILE_DIRECTORY"></span>**arquivo/diretório completo**
</dt>
<dd>

Um arquivo ou diretório que foi criado no sistema de arquivos local ou um arquivo que foi modificado, fazendo com que ele não seja mais um cache de seu estado no repositório de backup.  Consulte [estado do cache na raiz de virtualização](cache-state.md).
</dd>

<dt>

<span id="projfs.glossary_hydrated_placeholder"></span><span id="PROJFS.GLOSSARY_HYDRATED_PLACEHOLDER"></span>**espaço reservado para alimentador**
</dt>
<dd>

Um arquivo cujo conteúdo e metadados foram armazenados em cache no disco.  Consulte [estado do cache na raiz de virtualização](cache-state.md).
</dd>

<dt>

<span id="projfs.glossary_placeholder"></span><span id="PROJFS.GLOSSARY_PLACEHOLDER"></span>**reservado**
</dt>
<dd>

Um arquivo ou diretório que não está totalmente presente no disco.  Consulte [estado do cache na raiz de virtualização](cache-state.md).
</dd>

<dt>

<span id="projfs.glossary_tombstone"></span><span id="PROJFS.GLOSSARY_TOMBSTONE"></span>**marca para exclusão**
</dt>
<dd>

Um espaço reservado especial oculto que representa um item que foi excluído do sistema de arquivos local.  Consulte [estado do cache na raiz de virtualização](cache-state.md).
</dd>

<dt>

<span id="projfs.glossary_virtual_file_directory"></span><span id="PROJFS.GLOSSARY_virtual_file_directory"></span>**arquivo/diretório virtual**
</dt>
<dd>

Um arquivo ou diretório que não existe fisicamente no disco, mas é projetado em resultados de enumeração.  Consulte [estado do cache na raiz de virtualização](cache-state.md).
</dd>

<dt>

<span id="projfs.glossary_virtualization_instance"></span><span id="PROJFS.GLOSSARY_VIRTUALIZATION_INSTANCE"></span>**instância de virtualização**
</dt>
<dd>

Um objeto na memória que gerencia a comunicação entre o provedor e o ProjFS para o conjunto de arquivos e diretórios localizados em uma raiz de virtualização específica.
</dd>

<dt>

<span id="projfs.glossary_virtualization_root"></span><span id="PROJFS.GLOSSARY_VIRTUALIZATION_ROOT"></span>**raiz de virtualização**
</dt>
<dd>

Um diretório no sistema de arquivos sob o qual os dados do provedor são projetados.
</dd>

</dl>

<!--
<dt>

<span id="projfs.glossary_"></span><span id="PROJFS.GLOSSARY_"></span>**TERM**
</dt>
<dd>

DEFINITION
</dd>
-->