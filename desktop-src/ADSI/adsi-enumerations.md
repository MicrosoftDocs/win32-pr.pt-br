---
title: Enumerações ADSI
description: As interfaces de serviço Active Directory (ADSI) definem e usam as enumerações listadas na tabela a seguir.
ms.assetid: f0ad5ce5-742d-40dc-ac5a-31d779e40bfd
ms.tgt_platform: multiple
keywords:
- ADSI, referência, enumerações ADSI
- ADSI de enumerações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c10d5aed5688e7128a64a32dee2f83efa22ab5bf292231517026299ccb592886
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023904"
---
# <a name="adsi-enumerations"></a>Enumerações ADSI

As interfaces de serviço Active Directory (ADSI) definem e usam as enumerações listadas na tabela a seguir.



| Enumeração                                                           | Descrição                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Enumeração do ADS \_ ACEFLAG \_**](/windows/win32/api/iads/ne-iads-ads_aceflag_enum)                        | Especifica como a segurança é propagada para ACEs (entradas de controle de acesso) herdadas e tipos de auditoria para uma ACE do sistema.                                                                                                                                             |
| [**Enumeração do ADS \_ ACETYPE \_**](/windows/win32/api/iads/ne-iads-ads_acetype_enum)                        | Especifica o tipo de ACE.                                                                                                                                                                                                                                           |
| [**\_enumeração de autenticação ADS \_**](/windows/win32/api/iads/ne-iads-ads_authentication_enum)          | Especifica o nível de segurança usado na autenticação de um cliente.                                                                                                                                                                                                     |
| [**Enumeração de referências do ADS \_ Chase \_ \_**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum)       | Especifica o comportamento da caça de referência.                                                                                                                                                                                                                       |
| [**\_DEREFENUM ADS**](/windows/win32/api/iads/ne-iads-ads_derefenum)                               | Especifica o comportamento da desreferência de alias.                                                                                                                                                                                                                    |
| [**\_enum de exibição de anúncios \_**](/windows/win32/api/iads/ne-iads-ads_display_enum)                        | Especifica como um caminho é exibido.                                                                                                                                                                                                                                |
| [**\_enumeração do \_ modo de escape do ADS \_**](/windows/win32/api/iads/ne-iads-ads_escape_mode_enum)               | Especifica se caracteres especiais são de escape, sem escape ou inalterados.                                                                                                                                                                                        |
| [**\_Enumeração flagType \_ ADS**](/windows/win32/api/iads/ne-iads-ads_flagtype_enum)                      | Especifica a presença dos campos **objecttype** ou **INHERITEDOBJECTTYPE** em uma ACE.                                                                                                                                                                         |
| [**\_enumeração de formato ADS \_**](/windows/win32/api/iads/ne-iads-ads_format_enum)                          | Especifica o tipo de valores em um objeto de nome de caminho.                                                                                                                                                                                                                |
| [**\_enumeração de \_ tipo de grupo ADS \_**](/windows/win32/api/iads/ne-iads-ads_group_type_enum)                 | Especifica o tipo de grupo do membro.                                                                                                                                                                                                                           |
| [**ADS \_ nome \_ inittype \_ enum**](/windows/win32/api/iads/ne-iads-ads_name_inittype_enum)           | Especifica o tipo de inicialização a ser executada em um objeto de conversão de nome.                                                                                                                                                                                  |
| [**nome do ADS \_ \_ tipo \_ enum**](/windows/win32/api/iads/ne-iads-ads_name_type_enum)                   | Especifica o formato usado para representar nomes distintos.                                                                                                                                                                                                       |
| [**\_enumeração da opção ADS \_**](/windows/win32/api/iads/ne-iads-ads_option_enum)                          | Especifica as opções disponíveis que a interface [**IADsObjectOptions**](/windows/desktop/api/Iads/nn-iads-iadsobjectoptions) usa para manipular objetos de diretório.                                                                                                                        |
| [**\_enumeração de \_ codificação de senha ADS \_**](/windows/win32/api/iads/ne-iads-ads_password_encoding_enum)   | Usado para identificar o tipo de codificação de senha usado com a opção de **\_ método de \_ senha \_ de opção ADS** nos métodos [**IADsObjectOptions:: GetOption**](/windows/desktop/api/Iads/nf-iads-iadsobjectoptions-getoption) e [**IADsObjectOptions:: SetOption**](/windows/desktop/api/Iads/nf-iads-iadsobjectoptions-setoption) . |
| [**\_Enumeração PathType de ADS \_**](/windows/win32/api/iads/ne-iads-ads_pathtype_enum)                      | Especifica o tipo de objeto no qual o descritor de segurança é modificado.                                                                                                                                                                                        |
| [**\_enumeração de preferências do ADS \_**](/windows/win32/api/iads/ne-iads-ads_preferences_enum)                | Especifica as preferências de consulta do OLE DB para ADSI.                                                                                                                                                                                                           |
| [**\_enumeração de \_ operação de propriedade ADS \_**](/windows/win32/api/iads/ne-iads-ads_property_operation_enum) | Especifica as maneiras de atualizar valores de propriedade no cache de propriedades.                                                                                                                                                                                               |
| [**\_enumeração de direitos de ADS \_**](/windows/win32/api/iads/ne-iads-ads_rights_enum)                          | Especifica os direitos de acesso a um objeto de serviço de diretório.                                                                                                                                                                                                        |
| [**\_SCOPEENUM ADS**](/windows/win32/api/iads/ne-iads-ads_scopeenum)                               | Especifica o escopo de uma pesquisa de diretório.                                                                                                                                                                                                                        |
| [**\_enumeração de \_ controle \_ SD de ADS**](/windows/win32/api/iads/ne-iads-ads_sd_control_enum)                 | Especifica que uma ACL (lista de controle de acesso) deve ser protegida quando novas permissões são aplicadas recursivamente a uma árvore de diretório.                                                                                                                                  |
| [**\_enumeração de \_ formato \_ SD de ADS**](/windows/win32/api/iads/ne-iads-ads_sd_format_enum)                   | Especifica o formato para converter o descritor de segurança.                                                                                                                                                                                                      |
| [**\_enumeração de \_ revisão \_ SD do ADS**](/windows/win32/api/iads/ne-iads-ads_sd_revision_enum)               | Especifica o número de revisão de uma ACE ou ACL.                                                                                                                                                                                                                   |
| [**Enumeração do ADS \_ SEARCHPREF \_**](/windows/win32/api/iads/ne-iads-ads_searchpref_enum)                  | Especifica as preferências da pesquisa.                                                                                                                                                                                                                              |
| [**\_enumeração de \_ informações de segurança do ADS \_**](/windows/win32/api/iads/ne-iads-ads_security_info_enum)           | Especifica as opções para examinar os dados de segurança.                                                                                                                                                                                                                |
| [**\_enumeração de tipo \_ ADS**](/windows/win32/api/iads/ne-iads-ads_settype_enum)                        | Especifica o formato de caminho em [**IADsPathname:: Set**](/windows/desktop/api/Iads/nf-iads-iadspathname-set).                                                                                                                                                                                       |
| [**\_STATUSENUM ADS**](/windows/win32/api/iads/ne-iads-ads_statusenum)                             | Especifica o status das preferências de pesquisa.                                                                                                                                                                                                                       |
| [**Enumeração do ADS \_ SYSTEMFLAG \_**](/windows/win32/api/iads/ne-iads-ads_systemflag_enum)                  | Especifica os tipos de atributos representados por um objeto **attributeSchema** .                                                                                                                                                                                   |
| [**\_enumeração de \_ sinalizador de usuário ADS \_**](/windows/win32/api/iads/ne-iads-ads_user_flag_enum)                   | Especifica os sinalizadores usados para manipular as propriedades do usuário.                                                                                                                                                                                                            |
| [**\_enumeração de DIALETO ADSI \_**](/windows/win32/api/iads/ne-iads-adsi_dialect_enum)                      | Especifica os dialetos de consulta ADSI disponíveis.                                                                                                                                                                                                                          |
| [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum)                                    | Especifica os tipos de dados usados para interpretar uma cadeia de caracteres de sintaxe estendida ADSI.                                                                                                                                                                                            |



 

## <a name="remarks"></a>Comentários

como os aplicativos do Visual Basic script Edition não podem ler dados de uma biblioteca de tipos, os aplicativos VBScript não podem reconhecer constantes simbólicas conforme definido nessas enumerações. Use as constantes numéricas em vez disso para definir os sinalizadores apropriados em aplicativos VBScript. Para usar as constantes simbólicas como uma boa prática de programação, grave declarações explícitas dessas constantes, como feito aqui, em aplicativos VBScript.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IADsObjectOptions**](/windows/desktop/api/Iads/nn-iads-iadsobjectoptions)
</dt> <dt>

[**IADsPathname:: Set**](/windows/desktop/api/Iads/nf-iads-iadspathname-set)
</dt> </dl>

 

 




