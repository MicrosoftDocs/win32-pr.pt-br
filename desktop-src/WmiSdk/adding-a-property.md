---
description: As propriedades nas classes WMI descrevem dados sobre um objeto gerenciado.
ms.assetid: 4046bfc7-9528-4737-ad61-bbb8419d0b51
ms.tgt_platform: multiple
title: Adicionando uma propriedade WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bba8944da155ca250edfed0c6e9160f555ba9551
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812262"
---
# <a name="adding-a-wmi-property"></a>Adicionando uma propriedade WMI

As propriedades nas classes WMI descrevem dados sobre um objeto gerenciado. Por exemplo, **HANDLE**, **ProcessId** e **PageFaults** são definidos como propriedades da classe de [**\_ processo do Win32**](/windows/desktop/CIMWin32Prov/win32-process) e descrevem aspectos de um processo do sistema operacional. Para obter mais informações, consulte [escrevendo um provedor de propriedades](writing-a-property-provider.md).

## <a name="defining-a-property-in-mof"></a>Definindo uma propriedade no MOF

Uma propriedade WMI representa um aspecto ou estado no objeto. Em vez de criar métodos que simplesmente obtêm e definem um valor, você pode criar uma propriedade. Por exemplo, a propriedade **netenabled** de [**\_ adaptador do Win32**](/windows/desktop/CIMWin32Prov/win32-networkadapter) exibe se o estado do adaptador está habilitado ou desabilitado. No entanto, os métodos [**Enable**](/windows/desktop/CIMWin32Prov/enable-method-in-class-win32-networkadapter) e [**Disable**](/windows/desktop/CIMWin32Prov/disable-method-in-class-win32-networkadapter) realmente executam a ação de alterar o estado do adaptador.

Uma propriedade deve ter um tipo de dados. O tipo de dados do **identificador** de Propriedade do [**\_ processo do Win32**](/windows/desktop/CIMWin32Prov/win32-process) é **String** e o tipo de dados de **PageFaults** é **UInt32**. Se uma propriedade puder ter apenas dois Estados, o tipo de dados da propriedade será normalmente definido como **booliano**.

A propriedade também pode ser uma matriz. Por exemplo, a propriedade **Sid**(identificador de segurança) [**do \_ confiança do Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) é uma matriz de bytes (**uint8**) que contém o Sid. As propriedades podem conter objetos incorporados que são referências a uma ou mais instâncias de outra classe WMI. A **DACL (** lista de controle de acesso discricionário) e as propriedades da **SACL (** lista de controle de acesso do sistema) do [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor), por exemplo, são matrizes de objetos do [**Win32 \_ Ace**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) que descrevem os grupos e contas que têm acesso. A propriedade **Group** no **Win32 \_ SecurityDescriptor** contém uma referência a uma única instância do **Win32 \_ Trustee**. Para obter mais informações, consulte [inserindo objetos em uma classe](embedded-objects.md).

Uma propriedade pode ter vários [*qualificadores*](gloss-q.md). Esses [qualificadores](wmi-qualifiers.md) podem ser [*modelo CIM (CIM)*](gloss-c.md) ou qualificadores WMI ou podem ser específicos para determinados tipos de classes, por exemplo, os qualificadores de classe do [contador de desempenho](qualifiers-specific-to-wmi-performance-classes.md) . Os qualificadores especificam algum aspecto da propriedade, como se for somente leitura ou se não puder ser alterado sem um privilégio específico. Um aplicativo que tenta gravar na propriedade **DACL** do [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor), por exemplo, requer os privilégios **SeSecurityPrivilege** e **SeRestorePrivilege**. Para obter mais informações, consulte [adicionando um qualificador](adding-a-qualifier.md).

Por fim, uma propriedade deve ter um nome. Você pode nomear uma propriedade de qualquer coisa dentro dos limites da prática de programação padrão. No entanto, há duas exceções principais. Primeiro, você não pode usar nenhuma palavra-chave MOF, como "Class", como um nome de propriedade. Em segundo lugar, você não pode usar nenhuma palavra-chave WQL, como "grupo", como um nome de propriedade. Para obter mais informações sobre as palavras-chave MOF e WQL, consulte [tipos de dados MOF](mof-data-types.md) e [WQL (SQL para WMI)](wql-sql-for-wmi.md).

Para o código do C++ e do formato MOF (MOF), você declara as propriedades de uma classe ao mesmo tempo em que declara a classe.

**Para definir uma propriedade**

-   Inclua o tipo de dados de propriedade, o nome e um valor padrão opcional e qualificador entre as chaves da descrição da classe.

    ``` syntax
    class MyClass 
    {
        [key] string   strProp;
        sint32         dwProp1 = 21;
        uint32         dwProp2;
    };
    ```

    A classe MyClass no exemplo anterior tem três propriedades: uma cadeia de caracteres, um inteiro com sinal de 32 bits e um inteiro sem sinal de 32 bits. Cada propriedade é atribuída a um nome que não diferencia maiúsculas de minúsculas e um tipo de dados MOF.

    O qualificador de [**chave**](key-qualifier.md) define a propriedade de cadeia de caracteres como a propriedade de chave que identifica exclusivamente uma instância da classe. Para obter mais informações sobre qualificadores, consulte [adicionando um qualificador](adding-a-qualifier.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando uma classe](creating-a-class.md)
</dt> </dl>

 

 
