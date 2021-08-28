---
description: Os provedores de WMI também podem manter logs. Quais arquivos de log aparecem em um sistema depende de quais provedores estão instalados.
ms.assetid: 04f041e5-4f2c-4c94-9aba-b040d941b46d
ms.tgt_platform: multiple
title: Arquivos de log do provedor WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed9cc74b9f1c6be16f1d85eb1e1863e0dc8b7b33
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880004"
---
# <a name="wmi-provider-log-files"></a>Arquivos de log do provedor WMI

Os provedores de WMI também podem manter logs. Quais arquivos de log aparecem em um sistema depende de quais provedores estão instalados.

Esses logs podem estar localizados no diretório% systemroot% \\ System32 \\ WBEM \\ logs.

-   [Wmiprov. log](#wmiprovlog)
-   [Ntevt. log](#ntevtlog)
-   [Dsprovider. log](#dsproviderlog)
-   [Tópicos relacionados](#related-topics)

## <a name="wmiprovlog"></a>Wmiprov. log

o arquivo Wmiprov. log contém dados de gerenciamento e eventos de drivers wdm (Windows Driver Model habilitados para WMI) e o [provedor wdm](/windows/desktop/WmiCoreProv/wdm-provider). Ele fornece informações de aviso e erro principalmente para solução de problemas e depuração do provedor e dos aplicativos cliente que o utilizam.

O wmiprov. log contém:

-   Erros do [provedor WDM](/windows/desktop/WmiCoreProv/wdm-provider) ou do driver de dispositivo, como a compilação binária de MOF com falha ou falha ao recuperar dados.
-   O status da compilação do MOF para cada um dos drivers que usam o formato MOF.
-   Eventos de construção e desconstrução do provedor.
-   Impressão de WNODE.

## <a name="ntevtlog"></a>Ntevt. log

O arquivo Ntevt. log contém mensagens de rastreamento do [provedor de log de eventos](/previous-versions/windows/desktop/eventlogprov/event-log-provider).

## <a name="dsproviderlog"></a>Dsprovider. log

O arquivo Dsprovider. log contém informações de rastreamento e mensagens de erro para o [provedor de Active Directory](/previous-versions/windows/desktop/dsprov/active-directory-provider).

A tabela a seguir lista alguns problemas comuns que podem ocorrer e oferece possíveis causas e soluções.



| Mensagem                                                                                                                                                                                                                                                                                                        | Descrição                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FALHA de CLDAPClassProvider:: InitializeLDAPProvider ADsGetObject em RootDSE: &lt; HRESULT&gt;                                                                                                                                                                                                                    | A chamada ADSI falhou ao tentar obter a raiz dos serviços de diretório. Verifique se o computador é membro de um domínio.                                                                                                                                                                                                                                                                             |
| CDSClassProvider:: GetObjectAsync () GetClassFromCacheOrADSI falhou por <class name> com &lt; HRESULT&gt;                                                                                                                                                                                                  | A classe que você está tentando obter não é uma classe válida no diretório. Verifique se o nome da classe está correto.                                                                                                                                                                                                                                                                                                |
| CLDAPInstanceProvider::P utInstanceAsync () falha de ModifyExistingInstance para LDAP:Binding = foo1, CN = Users, DC = dsprovider, DC = nttest, DC = Microsoft, DC = com com &lt; HRESULT&gt;                                                                                                                                       | O provedor não pôde gravar uma instância modificada nos serviços de diretório. Verifique se você está usando a interface [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) para especificar o conjunto de propriedades que você está modificando. Para obter mais informações sobre como usar a interface **IWbemContext** com [**PutInstance**](/windows/desktop/api/Provider/nf-provider-provider-putinstance(constcinstance__long)), consulte [atualizando uma instância inteira](updating-an-entire-instance.md). |
| CLDAPHelper:: GetADSIInstance ADsOpenObject () falhou <class name> com &lt; HRESULT&gt;<br/> CLDAPInstanceProvider:: GetObjectAsync: GetADSIInstance () falhou com &lt; HRESULT&gt;<br/> CLDAPInstanceProvider:: GetObjectAsync () falhou para o \_ usuário DS. ADSIPath = "<class name><br/> | Essas três mensagens indicam que a instância que você está tentando obter não existe no serviço de diretório. Verifique se o valor **ADSIPath** e o nome da classe estão corretos.                                                                                                                                                                                                                                |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Arquivos de log do WMI](wmi-log-files.md)
</dt> </dl>

 

