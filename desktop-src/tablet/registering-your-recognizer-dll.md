---
description: A DLL do reconhecedor deve ser registrada para a Plataforma de Tablet PC usá-la. O reconhecedor deve fazer as seguintes alterações no Registro na instalação.
ms.assetid: 1f1d826b-3968-424b-8da8-b69590058ff1
title: Registrando sua DLL do Reconhecedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae80eb49f1795e315cf77bf5aede83cc1677e168f4aea4d6715a216e74434caf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119350066"
---
# <a name="registering-your-recognizer-dll"></a>Registrando sua DLL do Reconhecedor

A DLL do reconhecedor deve ser registrada para a Plataforma de Tablet PC usá-la. O reconhecedor deve fazer as seguintes alterações no Registro na instalação.

Adicione uma nova chave para cada uma das CLSIDs do reconhecedor na chave do Registro HKEY \_ LOCAL \_ MACHINE/SOFTWARE/Microsoft/TPG/Recognizers/. Adicione um CLSID por idioma. A tabela a seguir descreve os valores que devem ser adicionados abaixo de cada uma das chaves que contêm suas CLSIDs.

> [!Note]  
> Os nomes desses valores são sensíveis a minúsculas.

 



| Nome do valor                             | Tipo de valor             | Descrição do valor                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Sinalizadores de capacidade do reconhecedor<br/> | REG \_ DWORD<br/>  | DWORD usado para determinar os recursos do reconhecedor.<br/>                                                                                                                                                                                                                                                                                                                             |
| DLL do Reconhecedor<br/>              | REG \_ SZ<br/>     | Caminho completo para a DLL do reconhecedor instalada.<br/>                                                                                                                                                                                                                                                                                                                                              |
| Idiomas reconhecidos<br/>        | REG \_ BINARY<br/> | Matriz binária que descreve o idioma ou os idiomas com os que um reconhecedor foi projetado para trabalhar.<br/> Em rectypes.h, a definição de MAX LANGUAGES especifica o número máximo de idiomas com suporte por um reconhecedor e cada idioma leva um WORD para armazenar no \_ item "Idiomas Reconhecidos". O tamanho da entrada do registro REG \_ BINARY deve ser MAX \_ LANGUAGES \* sizeof(WORD).<br/> |



 

 

 




