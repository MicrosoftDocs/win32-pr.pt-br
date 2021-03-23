---
title: Assinaturas raiz
description: A assinatura raiz define quais tipos de recursos estão associados ao pipeline de gráficos.
ms.assetid: ee32a222-8469-4af5-b688-afa70cf77c6a
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf4c034e208dd841545777cc92878e7020b9b4a7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548269"
---
# <a name="root-signatures"></a>Assinaturas raiz

A assinatura raiz define quais tipos de recursos estão associados ao pipeline de gráficos.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                               | Descrição                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Visão geral das assinaturas raiz](root-signatures-overview.md)<br/>                                                 | Uma assinatura de raiz é configurada pelas listas de comandos de aplicativo e links para os recursos que os sombreadores precisam. A lista de comandos de gráficos tem uma assinatura de raiz de computação e de elementos gráficos. Uma lista de comandos de computação terá apenas uma assinatura de raiz de computação. Essas assinaturas raiz são independentes umas das outras.<br/>                                                                                             |
| [Usando uma assinatura de raiz](using-a-root-signature.md)<br/>                                                     | A assinatura raiz é a definição de uma coleção organizada arbitrariamente de tabelas de descritores (incluindo seu layout), constantes raiz e descritores raiz. Cada entrada tem um custo em direção a um limite máximo, portanto, o aplicativo pode compensar o equilíbrio entre o número de cada tipo de entrada que a assinatura raiz conterá.<br/>                                                                     |
| [Criando uma assinatura raiz](creating-a-root-signature.md)<br/>                                               | As assinaturas raiz são uma estrutura de dados complexa que contém estruturas aninhadas. Eles podem ser definidos programaticamente usando a definição de estrutura de dados abaixo (que inclui métodos para ajudar a inicializar Membros). Como alternativa, eles podem ser criados na HLSL (linguagem de sombreamento de alto nível), dando a vantagem de que o compilador será validado antes que o layout seja compatível com o sombreador. <br/> |
| [Limites de assinatura raiz](root-signature-limits.md)<br/>                                                       | A assinatura raiz é a principal imobiliária e há limites e custos rígidos a serem considerados.<br/>                                                                                                                                                                                                                                                                                                            |
| [Usando constantes diretamente na assinatura raiz](using-constants-directly-in-the-root-signature.md)<br/>     | Os aplicativos podem definir constantes raiz na assinatura raiz, cada uma como um conjunto de valores de 32 bits. Eles aparecem na HLSL (linguagem de sombreamento de alto nível) como um buffer constante. Observe que os buffers de constante por motivos históricos são exibidos como conjuntos de valores de 4x32 bits. <br/>                                                                                                                                        |
| [Usando descritores diretamente na assinatura raiz](using-descriptors-directly-in-the-root-signature.md)<br/> | Os aplicativos podem colocar os descritores diretamente na assinatura raiz para evitar ter de passar por um heap de descritor. Esses descritores demoram muito espaço na assinatura raiz (consulte a seção limites de assinatura raiz), de modo que os aplicativos precisam usá-los com moderação. <br/>                                                                                                                                     |
| [Exemplo de assinaturas raiz](example-root-signatures.md)<br/>                                                   | A seção a seguir mostra as assinaturas raiz que variam em complexidade de vazia para completamente completa.<br/>                                                                                                                                                                                                                                                                                                       |
| [Especificando assinaturas raiz em HLSL](specifying-root-signatures-in-hlsl.md)<br/>                             | A especificação de assinaturas raiz no modelo do sombreador HLSL 5,1 é uma alternativa para especificá-los no código C++.<br/>                                                                                                                                                                                                                                                                                                  |
| [Assinatura de raiz versão 1,1](root-signature-version-1-1.md)<br/>                                             | A finalidade da assinatura de raiz versão 1,1 é permitir que os aplicativos indiquem os drivers quando os descritores em um heap de descritor não forem alterados nem os descritores de dados apontarem para uma alteração de t. Isso permite que a opção de drivers crie otimizações que podem ser possíveis de saber que um descritor ou a memória apontada por ele é estático por um período de tempo. <br/>                                  |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature)
</dt> <dt>

[**ID3D12RootSignatureDeserializer**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignaturedeserializer)
</dt> <dt>

[Associação de recursos](resource-binding.md)
</dt> </dl>

 

