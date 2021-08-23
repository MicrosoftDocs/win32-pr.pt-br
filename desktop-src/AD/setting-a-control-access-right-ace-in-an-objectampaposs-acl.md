---
title: Definindo um ACE direito de acesso de controle na ACL de um objeto
description: Usando ADSI, você definirá um ACE direito de acesso de controle, assim como faria com uma ACE específica da propriedade, exceto que a propriedade IADsAccessControlEntry.ObjectType é o rightsGUID do direito de acesso de controle.
ms.assetid: 454dc372-47b0-457d-8660-644fcfa59be8
ms.tgt_platform: multiple
keywords:
- Definindo um ACE direito de acesso de controle na ACL de um objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09f4a4406bfa3d16a3e3be228bf4a0f131d77ad68cb99a6b9b2a8d328f15215e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024804"
---
# <a name="setting-a-control-access-right-ace-in-an-objects-acl"></a>Definindo um ACE direito de acesso de controle na ACL de um objeto

Usando a ADSI, você definirá um ACE direito de acesso de controle, assim como faria com uma ACE específica da propriedade, exceto que a propriedade [**IADsAccessControlEntry.ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) é o **rightsGUID** do direito de acesso de controle. Esteja ciente de que você também pode usar as APIs de segurança do Win32 para definir ACLs em objetos de diretório.

A tabela a seguir lista as [**propriedades IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) para direitos de acesso de controle que podem ser usados para definir propriedades para uma ACE.



| Propriedade                                                       | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Accessmask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) | Para controlar direitos de acesso que controlam o acesso de direitos estendidos a operações especiais, o AccessMask deve conter o **sinalizador ADS \_ RIGHT \_ DS CONTROL \_ \_ ACCESS.** Para direitos de acesso de controle que definem um conjunto de propriedades, AccessMask contém **ADS \_ RIGHT \_ DS READ \_ \_ PROP** e/ou **ADS RIGHT \_ \_ DS WRITE \_ \_ PROP**.<br/> Para direitos de acesso de controle que controlam gravações validadas, [**AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) contém **ADS RIGHT \_ \_ DS \_ SELF.**<br/> |
| [**Sinalizadores**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods)      | Esse valor deve incluir o **sinalizador ADS FLAG OBJECT TYPE \_ \_ \_ \_ PRESENT.**                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) | Esse valor deve ser o [**formato StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) do atributo **rightsGUID** do direito de acesso de controle. Esteja ciente de que, em uma ACE, a cadeia de caracteres GUID deve incluir as chaves de início e término, mesmo que o atributo **rightsGUID** do objeto **controlAccessRight** não inclua as chaves.                                                                                                                                     |
| [**Acetype**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods)    | ADS **\_ ACETYPE \_ ACCESS ALLOWED \_ \_ OBJECT** para conceder ao objeto de confiança o direito de controle de acesso ou **ADS \_ ACETYPE ACCESS \_ \_ DENIED \_ OBJECT** para negar ao objeto de confiança o direito de acesso de controle.                                                                                                                                                                                                                                                                                                     |
| [**Administrador**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods)    | A entidade de segurança, por exemplo, usuário, grupo, computador e assim por diante, à qual a ACE se aplica.                                                                                                                                                                                                                                                                                                                                                                                              |



 

Para obter mais informações sobre como criar uma ACE, consulte [Configurando direitos de acesso em um objeto](setting-access-rights-on-an-object.md).

Para obter mais informações e um exemplo de código para definir uma ACE, consulte Código de exemplo para definir uma [ACE em um objeto de diretório](example-code-for-setting-an-ace-on-a-directory-object.md).

 

