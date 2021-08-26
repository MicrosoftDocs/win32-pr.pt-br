---
description: Os provedores WMI também podem manter logs. Quais arquivos de log aparecem em um sistema depende de quais provedores estão instalados.
ms.assetid: 04f041e5-4f2c-4c94-9aba-b040d941b46d
ms.tgt_platform: multiple
title: Arquivos de log do provedor WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea35a4841d86de06abe56d894e0570ef20456a78d24ce83c3fe6039cb4e2a67c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030306"
---
# <a name="wmi-provider-log-files"></a>Arquivos de log do provedor WMI

Os provedores WMI também podem manter logs. Quais arquivos de log aparecem em um sistema depende de quais provedores estão instalados.

Esses logs podem estar localizados no diretório %systemroot% \\ system32 \\ wbem \\ logs.

-   [Wmiprov.log](#wmiprovlog)
-   [Ntevt.log](#ntevtlog)
-   [Dsprovider.log](#dsproviderlog)
-   [Tópicos relacionados](#related-topics)

## <a name="wmiprovlog"></a>Wmiprov.log

O arquivo Wmiprov.log contém dados de gerenciamento e eventos de drivers WDM (modelo de driver de Windows) habilitados para WMI e o [provedor WDM](/windows/desktop/WmiCoreProv/wdm-provider). Ele fornece informações de aviso e erro principalmente para solucionar problemas e depurar o provedor e os aplicativos cliente que as usam.

O Wmiprov.log contém:

-   Erros do Provedor [WDM](/windows/desktop/WmiCoreProv/wdm-provider) ou do driver de dispositivo, como falha na compilação MOF binária ou falha ao recuperar dados.
-   O status da compilação MOF para cada um dos drivers que usam o formato MOF.
-   Eventos de construção e desconstrução do provedor.
-   Impressão do WNODE.

## <a name="ntevtlog"></a>Ntevt.log

O arquivo Ntevt.log contém mensagens de rastreamento do Provedor [de Log de Eventos](/previous-versions/windows/desktop/eventlogprov/event-log-provider).

## <a name="dsproviderlog"></a>Dsprovider.log

O arquivo Dsprovider.log contém informações de rastreamento e mensagens de erro para o [Provedor do Active Directory](/previous-versions/windows/desktop/dsprov/active-directory-provider).

A tabela a seguir lista alguns problemas comuns que podem ocorrer e oferecem possíveis causas e soluções.



| Mensagem                                                                                                                                                                                                                                                                                                        | Descrição                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CLDAPClassProvider::InitializeLDAPProvider ADsGetObject em RootDSE FAILED: <hresult>                                                                                                                                                                                                                    | A chamada ADSI falhou ao tentar obter a raiz dos serviços de diretório. Verifique se o computador é membro de um domínio.                                                                                                                                                                                                                                                                             |
| CDSClassProvider::GetObjectAsync() GetClassFromCacheOrADSI FAILED for <class name> with <hresult>                                                                                                                                                                                                  | A classe que você está tentando obter não é uma classe válida no diretório . Verifique se o nome da classe está correto.                                                                                                                                                                                                                                                                                                |
| CLDAPInstanceProvider::P utInstanceAsync() ModifyExistingInstance FAILED for LDAP://CN=foo1, CN=Users, DC=dsprovider,DC=nttest, DC=Microsoft, DC=com <hresult>                                                                                                                                       | O provedor não pôde gravar uma instância modificada nos serviços de diretório. Verifique se você está usando a interface [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) para especificar o conjunto de propriedades que você está modificando. Para obter mais informações sobre como usar a interface **IWbemContext** com [**PutInstance**](/windows/desktop/api/Provider/nf-provider-provider-putinstance(constcinstance__long)), consulte [Atualizando uma instância inteira.](updating-an-entire-instance.md) |
| CLDAPHelper::GetADSIInstance ADsOpenObject() FALHOU <class name> com <hresult><br/> CLDAPInstanceProvider::GetObjectAsync : GetADSIInstance() FAILED com <hresult><br/> CLDAPInstanceProvider::GetObjectAsync() FAILED para o usuário \_ ds. ADSIPath="<class name><br/> | Essas três mensagens indicam que a instância que você está tentando obter não existe no serviço de diretório. Verifique se o **valor ADSIPath** e o nome da classe estão corretos.                                                                                                                                                                                                                                |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Arquivos de log WMI](wmi-log-files.md)
</dt> </dl>

 

