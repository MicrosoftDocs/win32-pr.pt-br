---
title: Definindo uma ACE Right de acesso de controle na ACL de um objeto
description: Usando o ADSI, você define um ACE de acesso de controle da mesma forma como faria com uma ACE específica de propriedade, exceto que a propriedade IADsAccessControlEntry. ObjectType é a rightsGUID do direito de acesso de controle.
ms.assetid: 454dc372-47b0-457d-8660-644fcfa59be8
ms.tgt_platform: multiple
keywords:
- Definindo uma ACE Right de acesso de controle na ACL de um objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f41b870ad3ed5432060fb51fe14c29a81ce4665
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103917105"
---
# <a name="setting-a-control-access-right-ace-in-an-objects-acl"></a>Definindo uma ACE Right de acesso de controle na ACL de um objeto

Usando o ADSI, você define um ACE de acesso de controle da mesma forma como faria com uma ACE específica de propriedade, exceto que a propriedade [**IADsAccessControlEntry. ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) é a **rightsGUID** do direito de acesso de controle. Lembre-se de que você também pode usar as APIs de segurança do Win32 para definir ACLs em objetos de diretório.

A tabela a seguir lista as propriedades [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) para controlar os direitos de acesso que podem ser usados para definir as propriedades de uma ACE.



| Propriedade                                                       | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) | Para controlar os direitos de acesso que controlam o acesso de direitos estendidos a operações especiais, o AccessMask deve conter o sinalizador de **\_ \_ \_ \_ acesso de controle DS direito do ADS** . Para controlar os direitos de acesso que definem um conjunto de propriedades, AccessMask contém **anúncios \_ Right \_ DS \_ Read \_ prop** e/ou **ADS \_ Right \_ DS \_ Write \_ prop**.<br/> Para controlar os direitos de acesso que controlam gravações validadas, a [**AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) contém **anúncios de \_ \_ \_ si próprio DS**.<br/> |
| [**Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods)      | Esse valor deve incluir o sinalizador de **\_ tipo de objeto sinalizador do ADS \_ \_ \_ presente** .                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) | Esse valor deve ser o formato [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) do atributo **rightsGUID** do direito de acesso de controle. Lembre-se de que, em uma ACE, a cadeia de caracteres GUID deve incluir as chaves de início e de término, mesmo que o atributo **rightsGUID** do objeto **controlAccessRight** não inclua as chaves.                                                                                                                                     |
| [**AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods)    | O **\_ objeto de \_ acesso \_ permitido \_ pelo ADS ACETYPE** para conceder ao objeto de controle de acesso o direito de acesso do Access ou do **ADS \_ ACETYPE \_ Access \_ negado \_** para negar o direito de acesso de controle de confiança.                                                                                                                                                                                                                                                                                                     |
| [**Confiança**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods)    | A entidade de segurança, por exemplo, usuário, grupo, computador e assim por diante, à qual a ACE se aplica.                                                                                                                                                                                                                                                                                                                                                                                              |



 

Para obter mais informações sobre como criar uma ACE, consulte [definindo direitos de acesso em um objeto](setting-access-rights-on-an-object.md).

Para obter mais informações e um exemplo de código para definir uma ACE, consulte [código de exemplo para definir uma ACE em um objeto de diretório](example-code-for-setting-an-ace-on-a-directory-object.md).

 

