---
description: Representa uma coleção de objetos ExtendedProperty.
ms.assetid: 9de25994-9f0b-47a0-b4c8-781aec782f88
title: Objeto ExtendedProperties
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperties
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0225582217df56f486a44f12e3ca6ea0003130fdb209fb67e9f9e4ee258764d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119007234"
---
# <a name="extendedproperties-object"></a>Objeto ExtendedProperties

\[CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use o PInvoke (Serviços de Invocação de Plataforma) para chamar a função de API Do Win32 [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) e obter as propriedades. Para obter informações sobre o PInvoke, consulte [Tutorial de invocação de plataforma.](https://msdn.microsoft.com/library/aa288468.aspx) O .NET e a CryptoAPI por meio de [P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) Parte 1 e .NET e CryptoAPI por meio de [P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subseções da parte 2 de Estender a criptografia do .NET com [CAPICOM e P/Invoke](/previous-versions/ms867087(v=msdn.10)) também podem ser úteis.\]

O **objeto ExtendedProperties** representa uma coleção de [**objetos ExtendedProperty.**](extendedproperty.md) Cada objeto representa uma única propriedade estendida.

## <a name="when-to-use"></a>Quando usar

O **objeto ExtendedProperties** é usado para executar as seguintes tarefas:

-   Adicione ou remova um [**objeto ExtendedProperty**](extendedproperty.md) da coleção.
-   Recupere o número de propriedades estendidas na coleção.
-   Recupere um [**objeto ExtendedProperty**](extendedproperty.md) específico da coleção.
-   Iterar pela coleção.

## <a name="members"></a>Membros

O **objeto ExtendedProperties** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#extendedproperties-object)

### <a name="methods"></a>Métodos

O **objeto ExtendedProperties** tem esses métodos.



| Método                                      | Descrição                                                                                    |
|:--------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**Adicionar**](extendedproperties-add.md)       | Adiciona um [**objeto ExtendedProperty**](extendedproperty.md) à coleção.<br/>      |
| [**Remover**](extendedproperties-remove.md) | Remove um [**objeto ExtendedProperty**](extendedproperty.md) da coleção.<br/> |



 

### <a name="properties"></a>Propriedades

O **objeto ExtendedProperties** tem essas propriedades.



| Propriedade                                                   | Tipo de acesso          | Descrição                                                                                                                                                                                                                     |
|:-----------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](extendedproperties-newenum.md)<br/> | Somente leitura<br/> | Recupera uma interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) em um objeto que pode ser usado para enumerar a coleção. Essa propriedade está oculta no Visual Basic Scripting Edition (VBScript).<br/> |
| [**Contagem**](extendedproperties-count.md)<br/>       | Somente leitura<br/> | Recupera o número de [**objetos ExtendedProperty**](extendedproperty.md) na coleção.<br/>                                                                                                                      |
| [**Item**](extendedproperties-item.md)<br/>         | Somente leitura<br/> | Recupera um [**objeto ExtendedProperty**](extendedproperty.md) que representa a propriedade estendida indexada da coleção. Essa é a propriedade padrão.<br/>                                                      |



 

## <a name="remarks"></a>Comentários

O **objeto ExtendedProperties** não pode ser criado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte ao cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte ao servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2.0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
