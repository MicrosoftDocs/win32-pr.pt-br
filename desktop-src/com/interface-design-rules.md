---
title: Regras de design de interface
description: Esta seção fornece um breve resumo das regras e diretrizes de design de interface.
ms.assetid: c43fc385-bcd6-45fc-91b2-ad9827fdb15c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58d11d55a1e24c02208ebeecddd5a4f90b8b01fa4a53444e6554cfcff37165f4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070806"
---
# <a name="interface-design-rules"></a>Regras de design de interface

Esta seção fornece um breve resumo das regras e diretrizes de design de interface. Algumas dessas regras são específicas para a arquitetura COM, enquanto outras são restrições impostas pela linguagem de design de interface, MIDL. Para obter detalhes sobre o design da interface COM, [consulte Anatomia de um arquivo IDL.](anatomy-of-an-idl-file.md)

Por definição, um objeto não é um objeto COM, a menos que implemente a interface [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) ou uma interface derivada de **IUnknown**. Além disso, as seguintes regras se aplicam a todas as interfaces implementadas em um objeto COM:

-   Eles devem ter um IID (identificador de interface exclusivo).
-   Eles devem ser imutáveis. Depois que eles são criados e publicados, nenhuma parte de sua definição pode mudar.
-   Todos os métodos de interface devem retornar um valor **HRESULT** para que as partes do sistema que lidam com o processamento remoto possam relatar erros de RPC.
-   Todos os parâmetros de cadeia de caracteres em métodos de interface devem ser Unicode.
-   Os tipos de dados devem ser remotamente remotamente. Se não for possível converter um tipo de dados em um tipo remotamente disponível, você terá que criar suas próprias rotinas de marshaling e desmarque. Além disso, **LPVOID** ou **\* void* _, não tem nenhum significado em um computador remoto. Use um ponteiro para [_ *IUnknown* *](/windows/desktop/api/Unknwn/nn-unknwn-iunknown), se necessário.

> [!Note]  
> A implementação atual de MIDL não lida com sobrecarga de função ou herança múltipla.

 

## <a name="other-interface-design-considerations"></a>Outras considerações de design de interface

Use ponteiros para dados com muito cuidado. Para criar os dados no espaço de endereço do processo chamado, o tempo de executar RPC deve saber o tamanho exato dos dados. Se, por exemplo, um **parâmetro CHAR \*** aponta para um buffer de caracteres em vez de um único caractere, os dados não podem ser re-criados corretamente. Use a sintaxe disponível com MIDL para descrever com precisão as estruturas de dados representadas por suas definições de tipo.

A inicialização é essencial para ponteiros que são inseridos em matrizes e estruturas e passados entre limites de processo. Os ponteiros não inicializados podem funcionar quando passados para um programa no mesmo espaço de processo, mas proxies e stubs pressuem que todos os ponteiros são inicializados com endereços válidos ou são nulos.

Tenha cuidado ao alias de ponteiros (permitindo que os ponteiros apontem para a mesma parte da memória). Se o alias for intencional, esses ponteiros deverão ser declarados como alias no arquivo IDL. Ponteiros declarados como não suavizados nunca devem ser alias uns aos outros.

Preste atenção em como alocar e liberar memória. Lembre-se de que, a menos que você diga explicitamente a um objeto COM (usando o atributo [**allocate)**](/windows/desktop/Midl/allocate) para não liberar uma estrutura de dados que foi criada durante uma chamada fora do processo, essa estrutura será destruída quando a chamada for concluída. Além disso, considere a sobrecarga potencialmente destrutiva criada pela alocação ineficiente de estruturas de dados que agora precisam ser empacotadas e desmarcadas.

Por fim, tenha cuidado ao definir os valores de retorno **HRESULT** para que você não crie códigos de erro que conflitam com códigos DE ITF de INSTALAÇÃO definidos pelo COM (valores entre 0x0000 e 0x01FF são reservados) ou que estão em conflito com outros \_ **valores HRESULT** com o mesmo valor. Sempre que possível, use os valores de retorno de êxito e falha COM universais e use um parâmetro [**out,**](/windows/desktop/Midl/out-idl) em vez de **um HRESULT**, para retornar informações específicas para a chamada de função.

Para obter mais informações, consulte estes tópicos:

-   [Projetando interfaces remotas](designing-remotable-interfaces.md)
-   [Usando uma interface COM](using-a-com-interface.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Definições de interface e bibliotecas de tipos](/windows/desktop/Midl/interface-definitions-and-type-libraries)
</dt> </dl>

 

 