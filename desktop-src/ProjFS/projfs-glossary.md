---
title: Windows Glossário do Sistema de Arquivos Projetado
description: Termos especiais usados no ProjFS.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: 12b6e90d98fce3882aa5dc8d552f88e9cd9f389d24673fdc5caf175e180082f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030976"
---
# <a name="windows-projected-file-system-glossary"></a>Windows Glossário do Sistema de Arquivos Projetado

Termos especiais usados no ProjFS.

<dl>
<dt>

<span id="projfs.glossary_backing_store"></span><span id="PROJFS.GLOSSARY_BACKING_STORE"></span>**armazenamento de backing**
</dt>
<dd>

Dados hierárquicos mantidos pelo provedor que são projetados no sistema de arquivos como arquivos e diretórios.
</dd>

<dt>

<span id="projfs.glossary_dirty_placeholder"></span><span id="PROJFS.GLOSSARY_DIRTY_PLACEHOLDER"></span>**espaço reservado sujo**
</dt>
<dd>

Um arquivo ou diretório que foi modificado localmente e não é mais um cache de seu estado no armazenamento do provedor.  Consulte [Estado do cache na Raiz de Virtualização.](cache-state.md)
</dd>

<dt>

<span id="projfs.glossary_full_file_directory"></span><span id="PROJFS.GLOSSARY_FULL_FILE_DIRECTORY"></span>**arquivo/diretório completo**
</dt>
<dd>

Um arquivo ou diretório que foi criado no sistema de arquivos local ou um arquivo que foi modificado, tornando-o não mais um cache de seu estado no armazenamento de back-back.  Consulte [Estado do cache na Raiz de Virtualização.](cache-state.md)
</dd>

<dt>

<span id="projfs.glossary_hydrated_placeholder"></span><span id="PROJFS.GLOSSARY_HYDRATED_PLACEHOLDER"></span>**espaço reservado dratado**
</dt>
<dd>

Um arquivo cujo conteúdo e metadados foram armazenados em cache em disco.  Consulte [Estado do cache na Raiz de Virtualização.](cache-state.md)
</dd>

<dt>

<span id="projfs.glossary_placeholder"></span><span id="PROJFS.GLOSSARY_PLACEHOLDER"></span>**Espaço**
</dt>
<dd>

Um arquivo ou diretório que não está totalmente presente no disco.  Consulte [Estado do cache na Raiz de Virtualização.](cache-state.md)
</dd>

<dt>

<span id="projfs.glossary_tombstone"></span><span id="PROJFS.GLOSSARY_TOMBSTONE"></span>**Lápide**
</dt>
<dd>

Um espaço reservado oculto especial que representa um item que foi excluído do sistema de arquivos local.  Consulte [Estado do cache na Raiz de Virtualização.](cache-state.md)
</dd>

<dt>

<span id="projfs.glossary_virtual_file_directory"></span><span id="PROJFS.GLOSSARY_virtual_file_directory"></span>**arquivo/diretório virtual**
</dt>
<dd>

Um arquivo ou diretório que não existe fisicamente no disco, mas é projetado em resultados de enumeração.  Consulte [Estado do cache na Raiz de Virtualização.](cache-state.md)
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