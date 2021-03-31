---
title: Invocando as DLLs de extensão
description: Chama essa função para cada pacote de autenticação ou contabilização válido que ele recebe do NAS (servidor de acesso à rede).
ms.assetid: 6d738ad7-cce5-4835-97d6-c57173c79a16
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bc96fab078a982f23f5f5dd86d51dbed46d5541
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917533"
---
# <a name="invoking-the-extension-dlls"></a>Invocando as DLLs de extensão

> [!Note]  
> O IAS (serviço de autenticação da Internet) foi renomeado como NPS (servidor de políticas de rede) a partir do Windows Server 2008. O conteúdo deste tópico aplica-se ao IAS e ao NPS. Em todo o texto, o NPS é usado para fazer referência a todas as versões do serviço, incluindo as versões originalmente chamadas de IAS.

 

As DLLs de extensão do NPS devem exportar pelo menos uma das seguintes funções de retorno de chamada: [*RadiusExtensionProcess*](/windows/desktop/api/authif/nc-authif-pradius_extension_process), [*RadiusExtensionProcessEx*](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex)ou [*RadiusExtensionProcess2*](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2). O NPS chama essas funções para cada pacote de autenticação ou contabilização válido que recebe do NAS (servidor de acesso à rede). O NPS chama essas funções em cada uma das DLLs listadas abaixo da [chave do registro de parâmetros](/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls)do NPS. As DLLs são chamadas na ordem em que são listadas.

Se uma DLL de extensão do NPS exportar mais de uma das funções acima, o NPS invocará apenas uma delas: a função mais recente com suporte do sistema operacional.

> [!Note]  
> Originalmente, o IAS suportava apenas [*RadiusExtensionProcess*](/windows/desktop/api/authif/nc-authif-pradius_extension_process). O IAS dá suporte também a [*RadiusExtensionProcessEx*](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex). O IAS (e o NPS posterior) também oferece suporte a [*RadiusExtensionProcess2*](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2).

 

As DLLs de extensão do NPS também podem exportar as funções [**RadiusExtensionInit**](/windows/desktop/api/authif/nc-authif-pradius_extension_init) e [**RadiusExtensionTerm**](/windows/desktop/api/authif/nc-authif-pradius_extension_term) . Se estiverem presentes, o NPS chamará essas funções quando o serviço for iniciado e interrompido, respectivamente.

## <a name="radiusextensionprocess-callback-function"></a>Função de retorno de chamada RadiusExtensionProcess

Em uma DLL de extensão de autenticação, o [*RadiusExtensionProcess*](/windows/desktop/api/authif/nc-authif-pradius_extension_process) recebe todos os atributos que são recebidos pelo NPS na solicitação de autenticação ou de contabilização. Usando esses atributos, a função pode executar validações adicionais, verificar as autorizações do usuário ou enviar registros de contabilidade para um servidor de Estado central.

Em uma DLL de extensão de autorização, o **RadiusExtensionProcess** recebe todos os atributos gerados pelo serviço de autorização do NPS. Esses são os atributos que são retornados no pacote Access-Accept.

Depois de chamar **RadiusExtensionProcess**, a ação executada pelo NPS depende do valor de retorno de **RadiusExtensionProcess** e do valor retornado no parâmetro *pfAction* . Esses valores são listados na tabela a seguir.



| *pfAction* | DLL de extensão de autenticação                                                                                                                                            | DLL de extensão de autorização                                                                                                                                 |
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Aceitar     | Ignora qualquer DLL de extensão de autenticação adicional e também ignora o mecanismo de autenticação NPS.                                                                  | Aceitar não permitido.                                                                                                                                         |
| Rejeitar     | Ignora qualquer DLL de extensão de autenticação adicional e também ignora o mecanismo de autenticação NPS. Access-Reject pacote é enviado.                                    | Ignora qualquer DLL de extensão de autorização adicional.                                                                                                          |
| Continuar   | O pacote será enviado para a próxima DLL de extensão de autenticação ou para o mecanismo de autenticação do NPS se não houver mais DLLs de extensão de autenticação listadas no registro. | O pacote será enviado para a próxima DLL de extensão de autorização ou para o log de contabilidade do NPS se não houver mais DLLs de extensão de autorização listadas no registro. |



 

Para todas as DLLs de extensão, se **RadiusExtensionProcess** retornar um erro, o pacote será Descartado. Os pacotes descartados devido a um erro não são processados pelo log de contabilidade do NPS.

Se ocorrer um erro, o NPS posta um evento de erro genérico no log de eventos. É recomendável que a DLL de extensão forneça log de erros adicional.

Para obter mais informações e um diagrama que representa o processo anterior, consulte [sobre as extensões do NPS](/windows/desktop/Nps/ias-about-internet-authentication-service).

**RadiusExtensionProcess** deverá retornar um erro se não for possível verificar a aceitação ou rejeição do pacote. Essa situação pode surgir se um problema de rede impedir que o **RadiusExtensionProcess** se comunique com seu banco de dados de autenticação de usuário.

Ao processar um pacote de estatísticas, o parâmetro *pfAction* é **nulo**, portanto *pfAction* não pode ser definido. Retornar um erro da função **RadiusExtensionProcess** durante o processamento de uma solicitação de contabilidade faz com que a solicitação seja descartada pelo NPS.

> [!Note]  
> Depois de receber uma aceitação, o NPS não chama **RadiusExtensionProcess** nas DLLs restantes na sequência. Como algumas funções de autenticação também podem implementar autorizações, ignorar essas funções de autenticação pode fazer com que as autorizações sejam omitidas. Se uma instância de [**RadiusExtensionProcess**](/windows/desktop/api/authif/nc-authif-pradius_extension_process) retornar Accept, é importante não fazer nenhuma suposição sobre as autorizações recuperadas.

 

Se continuar ou aceitar for retornado, o perfil correspondente ao Realm será enviado de volta no pacote de Access-Accept.

As DLLs de extensão de autenticação devem ser projetadas para coexistir com os provedores internos de autenticação do NPS e com outras DLLs de extensão. Se uma extensão for aplicável somente a um determinado banco de dados de usuário (por exemplo, Windows Active Directory), ela deverá verificar o atributo [**ratProvider**](/windows/desktop/api/authif/ne-authif-radius_authentication_provider) passado no parâmetro *pAttrs* , antes de processar a solicitação. O atributo ratProvider seria uma lista de atributos apontados pelo parâmetro *pAttrs* .

DLLs de extensão não devem rejeitar solicitações porque os atributos necessários estão ausentes. Por exemplo, se uma extensão de autenticação exigir o atributo User-Password, ratUserPassword e o atributo não estiver presente, a extensão deverá retornar uma ação de raContinue para fornecer a outras extensões e provedores a oportunidade de processar a solicitação.

O NPS chama a função [**RadiusExtensionProcess**](/windows/desktop/api/authif/nc-authif-pradius_extension_process) depois que a decisão de usar um determinado banco de dados de autenticação é feita, mas antes de o usuário ser autenticado. Portanto, as informações sobre qual banco de dados de autenticação usar está disponível para a função, para que a função possa verificar as autorizações do usuário no banco de dados de autenticação apropriado. O NPS dá suporte a vários bancos de dados de autenticação, incluindo o Active Directory do Windows.

## <a name="radiusextensionprocessex-callback-function"></a>Função de retorno de chamada RadiusExtensionProcessEx

As DLLs de extensão do NPS podem exportar [**RadiusExtensionProcessEx**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex) em vez de, ou além de, [**RadiusExtensionProcess**](/windows/desktop/api/authif/nc-authif-pradius_extension_process). Essa função permite que a DLL acrescente atributos de autorização adicionais à resposta de autenticação.

As mesmas informações descritas na seção *função de retorno de chamada RadiusExtensionProcess* aplicam-se à função [**RadiusExtensionProcessEx**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex) .

[**RadiusExtensionProcessEx**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex) não pode modificar ou remover nenhum dos atributos presentes. Se ocorrer um cenário no qual a DLL deve modificar ou remover atributos, a única opção é usar a interface do usuário do NPS para garantir que os atributos não estejam presentes. Por padrão, nenhum atributo de autorização está presente. Qualquer um que esteja presente deve ter sido adicionado por meio da interface do usuário.

Se várias DLLs de autorização estiverem configuradas e algumas dessas DLLs implementarem [**RadiusExtensionProcessEx**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex), a função **RadiusExtensionProcess/ex** em uma determinada dll não receberá os atributos das DLLs de autorização anteriormente chamadas. Ele recebe apenas os atributos gerados pelo serviço de autorização do NPS.

## <a name="radiusextensionprocess2-callback-function"></a>Função de retorno de chamada RadiusExtensionProcess2

As DLLs de extensão do NPS também podem exportar [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2) em vez de, ou além de, [**RadiusExtensionProcess**](/windows/desktop/api/authif/nc-authif-pradius_extension_process) e **RadiusExtensionProcessEx**. Essa função permite que a DLL adicione, modifique e remova atributos de e para a solicitação ou resposta de autenticação.

As mesmas informações descritas na seção *função de retorno de chamada RadiusExtensionProcessEx* aplicam-se à função [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex) , com as seguintes exceções:

-   Em uma DLL de autorização, o **RadiusExtensionProcess2** recebe os atributos gerados pelo serviço de autorização do NPS e os atributos gerados a partir de DLLs de autorização anteriormente chamadas.
-   [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2) não tem um parâmetro *pfAction* . **RadiusExtensionProcess2** define a disposição final da solicitação usando a função [**setresponsetype**](/previous-versions/ms688462(v=vs.85)) fornecida na estrutura do [**\_ bloco de \_ controle \_ de extensão RADIUS**](/windows/desktop/api/authif/ns-authif-radius_extension_control_block) .
-   O NPS sempre chama a função [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2) em qualquer DLL restante, independentemente de as funções nas DLLs anteriores retornarem Accept.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Configurando as DLLs de extensão](/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls)
</dt> <dt>

[Atributos de identificação de usuário](/windows/desktop/Nps/ias-user-identification-attributes)
</dt> </dl>

 

 