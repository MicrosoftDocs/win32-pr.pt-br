---
description: A partir do Windows 7, Instrumentação de Gerenciamento do Windows (WMI) implementou um mecanismo padrão para descobrir perfis usando o esquema CIM.
ms.assetid: e748b623-5ff3-464d-ba09-96cf226de7b6
ms.tgt_platform: multiple
title: Passagem de associação entre namespaces
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fe2bbb408c4d89a7093adf45f3daf276df294ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827844"
---
# <a name="cross-namespace-association-traversal"></a>Passagem de associação entre namespaces

A partir do Windows 7, Instrumentação de Gerenciamento do Windows (WMI) implementou um mecanismo padrão para descobrir perfis usando o esquema CIM.

O WMI dá suporte à passagem de associação entre namespaces e ao registro de perfil de associação. Para obter mais informações sobre o registro de perfil e a implementação padrão de CIM de passagem de associação, consulte DSP1033 ( [https://www.dmtf.org/standards/published\_documents/DSP1033.pdf](https://www.dmtf.org/sites/default/files/standards/documents/DSP1033_1.0.0.pdf) )

Para dar suporte a esse recurso, a infraestrutura do WMI fez o seguinte:

-   Criou o namespace Interop: \\ root \\ Interop.
-   Passagem de associação entre namespaces permitidas. Associações que cruzam namespaces dão suporte à filtragem no nível de classe de associação e no nível de namespace implementado.
-   Adicionadas as classes [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)), [**CIM \_ ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile)e [**CIM \_ ReferencedProfile**](cim-referencedprofile.md) .
-   Implementação da compatibilidade de 2.17.1 da versão do esquema CIM implementada. Para obter mais informações, consulte [compatibilidade do esquema CIM](cim-schema-compatibility.md).

## <a name="interop-namespace"></a>Namespace de interoperabilidade

O namespace Interop fornece um local comum para um aplicativo cliente descobrir todos os perfis com suporte em um computador. Os perfis podem ser usados para gerenciar vários aspectos de um sistema operacional, matriz de armazenamento ou banco de dados.

Todos os objetos e classes de interoperabilidade devem ser definidos no \\ namespace de interoperabilidade raiz.

## <a name="cim-classes"></a>Classes CIM

As classes CIM descritas na lista a seguir dão suporte à passagem de associação entre namespaces.

<dl> <dt>

<span id="CIM_RegisteredProfile"></span><span id="cim_registeredprofile"></span><span id="CIM_REGISTEREDPROFILE"></span>[**\_REGISTEREDPROFILE CIM**](/previous-versions//ee309375(v=vs.85))
</dt> <dd>

Usado para identificar a especificação de perfil que é anunciada como sendo implementada. Essa classe especifica informações que incluem o nome do perfil, a organização e a versão com a qual a implementação é compatível.

</dd> <dt>

<span id="CIM_ElementConformsToProfile"></span><span id="cim_elementconformstoprofile"></span><span id="CIM_ELEMENTCONFORMSTOPROFILE"></span>[**\_ELEMENTCONFORMSTOPROFILE CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile)
</dt> <dd>

Usado para associar instâncias de elementos de gerenciamento que são definidos em perfis com a classe [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) que identifica as especificações de perfil específicas que são implementadas.

</dd> <dt>

<span id="CIM_ReferencedProfile"></span><span id="cim_referencedprofile"></span><span id="CIM_REFERENCEDPROFILE"></span>[**\_REFERENCEDPROFILE CIM**](cim-referencedprofile.md)
</dt> <dd>

Usado para representar a relação entre os perfis.

</dd> </dl>

## <a name="implementing-cross-namespace-association-traversal"></a>Implementando a passagem de associação entre namespaces

O serviço WMI permite a passagem de associação entre namespaces. O WMI fornece o namespace Interop para registrar perfis e associá-los a perfis que são implementados em namespaces diferentes. No entanto, para usar a passagem de associação, os implementadores devem instanciar as classes de perfil na interoperabilidade e no namespace implementado. Para obter mais informações, consulte [escrevendo um provedor de associação para interoperabilidade](writing-an-association-provider-for-interop.md).

Associações que cruzam namespaces dentro do mesmo ambiente de gerenciamento devem ser instanciadas nos namespaces Interop e implemented. Caso contrário, a passagem de associação não funcionará. Por exemplo, o provedor de associação do perfil de energia deve ser registrado com os namespaces de raiz/interoperabilidade e raiz/cimv2/energia. A passagem de associação deve ser capaz de ocorrer de um namespace de volta para o outro. Para obter exemplos de passagem de associação, consulte [acessando dados no namespace Interop](accessing-data-in-the-interop-namespace.md).

* * Windows Vista: * *

Após a atualização para o Windows 7, se houver perfis de dispositivo de interoperabilidade instalados anteriormente no namespace de raiz/interoperabilidade, nenhum perfil do Windows 7 será instalado. Esses objetos de perfil de terceiros substituem o esquema de interoperabilidade do Windows 7 para manter a funcionalidade. Além disso, a ID de evento 5631 do aplicativo WMI é registrada.

Para obter os perfis de interoperabilidade do Windows 7, a versão do Windows 7 do arquivo Interop. mof e os arquivos MFL relacionados devem ser compilados. Para obter mais informações, consulte [compilando arquivos MOF](compiling-mof-files.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**\_REGISTEREDPROFILE CIM**](/previous-versions//ee309375(v=vs.85))
</dt> <dt>

[**\_ELEMENTCONFORMSTOPROFILE CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile)
</dt> <dt>

[**\_REFERENCEDPROFILE CIM**](cim-referencedprofile.md)
</dt> <dt>

[Compatibilidade do esquema CIM](cim-schema-compatibility.md)
</dt> <dt>

[Escrevendo um provedor de associação para interoperabilidade](writing-an-association-provider-for-interop.md)
</dt> <dt>

[Acessando dados no namespace Interop](accessing-data-in-the-interop-namespace.md)
</dt> </dl>

 

 
