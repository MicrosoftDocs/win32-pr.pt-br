---
title: Regras de design de interface
description: Esta seção fornece um breve resumo das regras e diretrizes de design de interface.
ms.assetid: c43fc385-bcd6-45fc-91b2-ad9827fdb15c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c1cde73527ac79a2e4442910e3053ed96748337
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104084915"
---
# <a name="interface-design-rules"></a>Regras de design de interface

Esta seção fornece um breve resumo das regras e diretrizes de design de interface. Algumas dessas regras são específicas para a arquitetura COM, enquanto outras são restrições impostas pela linguagem de design da interface, MIDL. Para obter detalhes do design da interface COM, consulte [anatomia de um arquivo IDL](anatomy-of-an-idl-file.md).

Por definição, um objeto não é um objeto COM, a menos que ele implemente a interface [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) ou uma interface derivada de **IUnknown**. Além disso, as seguintes regras se aplicam a todas as interfaces implementadas em um objeto COM:

-   Eles devem ter um IID (identificador de interface exclusivo).
-   Eles devem ser imutáveis. Depois que eles são criados e publicados, nenhuma parte de sua definição pode ser alterada.
-   Todos os métodos de interface devem retornar um valor **HRESULT** para que as partes do sistema que manipulam o processamento remoto possam relatar erros de RPC.
-   Todos os parâmetros de cadeia de caracteres em métodos de interface devem ser Unicode.
-   Seus tipos de dados devem ser remotos. Se não for possível converter um tipo de dados em um tipo remoto, você precisará criar suas próprias rotinas de empacotamento e desempacotamento. Além disso, **LPVOID**, **ou \* void**, não tem significado em um computador remoto. Use um ponteiro para [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown), se necessário.

> [!Note]  
> A implementação atual do MIDL não trata da sobrecarga de função ou de várias heranças.

 

## <a name="other-interface-design-considerations"></a>Outras considerações de design de interface

Use ponteiros para dados com muito cuidado. Para recriar os dados no espaço de endereço do processo que é chamado, o tempo de execução de RPC deve saber o tamanho exato dos dados. Se, por exemplo, um **parâmetro \* Char** apontar para um buffer de caracteres em vez de um único caractere, os dados não poderão ser recriados corretamente. Use a sintaxe disponível com MIDL para descrever com precisão as estruturas de dados representadas pelas suas definições de tipo.

A inicialização é essencial para ponteiros inseridos em matrizes e estruturas e passadas entre limites de processo. Ponteiros não inicializados podem funcionar quando passados para um programa no mesmo espaço de processo, mas proxies e stubs supõem que todos os ponteiros são inicializados com endereços válidos ou são nulos.

Tenha cuidado ao fazer o alias de ponteiros (permitindo que os ponteiros apontem para a mesma parte da memória). Se a alias for intencional, esses ponteiros devem ser declarados com alias no arquivo IDL. Ponteiros declarados como sem alias nunca devem ser alias uns aos outros.

Preste atenção em como alocar e liberar memória. Lembre-se de que, a menos que você explicitamente diga a um objeto COM (usando o atributo [**ALLOCATE**](/windows/desktop/Midl/allocate) ) para não liberar uma estrutura de dados que foi criada durante uma chamada fora do processo, essa estrutura será destruída quando a chamada for concluída. Além disso, considere a sobrecarga potencialmente destrutiva criada por alocação ineficiente de estruturas de dados que agora precisam ser empacotadas e desempacotadas.

Por fim, tenha cuidado ao definir os valores de retorno de **HRESULT** para que você não crie códigos de erro que estejam em conflito com os códigos de ITF de recursos definidos pelo com \_ (os valores entre 0x0000 e 0x01FF são reservados) ou que estejam em conflito com outros valores **HRESULT** com o mesmo valor. Sempre que possível, use os valores de retorno COM êxito e falha do universal COM e use um parâmetro [**out**](/windows/desktop/Midl/out-idl) , em vez de um **HRESULT**, para retornar informações específicas para a chamada de função.

Para mais informações, consulte os seguintes tópicos:

-   [Projetando interfaces remotas](designing-remotable-interfaces.md)
-   [Usando uma interface COM](using-a-com-interface.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Definições de interface e bibliotecas de tipos](/windows/desktop/Midl/interface-definitions-and-type-libraries)
</dt> </dl>

 

 