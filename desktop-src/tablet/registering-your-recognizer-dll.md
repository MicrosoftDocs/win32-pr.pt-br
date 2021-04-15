---
description: A DLL do reconhecedor deve ser registrada para que a plataforma do Tablet PC o use. O reconhecedor deve fazer as seguintes alterações no registro na instalação.
ms.assetid: 1f1d826b-3968-424b-8da8-b69590058ff1
title: Registrando a DLL do reconhecedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51114f11868e6d45dc4d319dab60e5b4f094ddbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506268"
---
# <a name="registering-your-recognizer-dll"></a>Registrando a DLL do reconhecedor

A DLL do reconhecedor deve ser registrada para que a plataforma do Tablet PC o use. O reconhecedor deve fazer as seguintes alterações no registro na instalação.

Adicione uma nova chave para cada um dos CLSIDs do reconhecedor na chave HKEY \_ local \_ /software/Microsoft/TPG/Recognizers/Registry. Adicione um CLSID por idioma. A tabela a seguir descreve os valores que devem ser adicionados abaixo de cada uma das chaves que contêm seus CLSIDs.

> [!Note]  
> Os nomes desses valores diferenciam maiúsculas de minúsculas.

 



| Nome do valor                             | Tipo de valor             | Descrição do valor                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Sinalizadores de capacidade do reconhecedor<br/> | REG \_ DWORD<br/>  | DWORD usado para determinar os recursos do reconhecedor.<br/>                                                                                                                                                                                                                                                                                                                             |
| DLL do reconhecedor<br/>              | REG \_ sz<br/>     | Caminho completo para a DLL do reconhecedor instalado.<br/>                                                                                                                                                                                                                                                                                                                                              |
| Idiomas reconhecidos<br/>        | \_binário reg<br/> | Matriz binária que descreve a linguagem ou os idiomas com os quais um reconhecedor foi projetado para trabalhar.<br/> Em recognizes. h, as \_ linguagens máximas definem especifica o número máximo de idiomas com suporte de um reconhecedor, e cada idioma usa uma palavra para armazenar no item "idiomas reconhecidos". O tamanho da entrada de \_ registro binário reg deve ser o \_ máximo \* de idiomas sizeof (Word).<br/> |



 

 

 




