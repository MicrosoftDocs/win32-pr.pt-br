---
title: Como solucionar problemas de erros de assinatura do pacote de aplicativos
description: Uma falha na implantação do aplicativo pode ser causada por uma falha ao validar a assinatura digital do pacote do aplicativo. Saiba como reconhecer essas falhas e o que fazer com elas.
ms.assetid: CE868296-87F6-4BD5-8AC5-914E429EDEBC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdec41d2d058a48153d6126fea534c1efaf16e16ccabef5d5e940daa73e839a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048944"
---
# <a name="how-to-troubleshoot-app-package-signature-errors"></a>Como solucionar problemas de erros de assinatura do pacote de aplicativos

Uma falha na implantação do aplicativo pode ser causada por uma falha ao validar a assinatura digital do pacote do aplicativo. Saiba como reconhecer essas falhas e o que fazer com elas.

Quando você implanta um aplicativo Windows empacotado, Windows sempre tenta validar a assinatura digital no pacote do aplicativo. Falhas durante a implantação do bloco de validação de assinatura do pacote. Mas o motivo pelo qual o pacote não foi validado pode não ser óbvio. Em particular, se você assinar seus pacotes com certificados privados para teste local, geralmente também deverá gerenciar a relação de confiança para esses certificados. Uma configuração de confiança de certificado incorreta pode levar a falhas de validação de assinatura.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Empacotamento, implantação e consulta de Windows aplicativos](appx-portal.md)
-   [Verificação de confiança de certificado](/windows/desktop/SecCrypto/certificate-trust-verification)

### <a name="prerequisites"></a>Pré-requisitos

-   [Windows Log de Eventos](/windows/desktop/WES/windows-event-log) para diagnosticar falhas de instalação.
-   [Tarefas certutil para gerenciar certificados para manipulação](/previous-versions/orphan-topics/ws.10/cc772898(v=ws.10)) de armazenamento de certificados durante a solução de problemas

## <a name="instructions"></a>Instruções

### <a name="step-1-examine-event-logs-for-diagnostic-information"></a>Etapa 1: Examinar os logs de eventos para obter informações de diagnóstico

Dependendo de como você tentou implantar seu aplicativo, talvez você não tenha recebido um código de erro significativo para a falha de implantação. Nesse caso, geralmente você pode obter o código de erro diretamente dos logs de eventos.

**Para obter o código de erro dos logs de eventos**

1.  Execute **eventvwr.msc**.
2.  Vá para **Visualizador de Eventos (Local)** Logs de Serviços e  >  **Aplicativos**  >  **da Microsoft**  >  **Windows**.
3.  O primeiro log a verificar é **AppxPackagingOM**  >  **Microsoft-Windows-AppxPackaging/Operational.**
4.  Erros relacionados à implantação são registrados **em AppXDeployment-Server**  >  **Microsoft-Windows-AppXDeploymentServer/Operational**.

    Para erros de implantação, pesquise o evento de erro 404 mais recente. Esse evento de erro fornece o código de erro e uma descrição do motivo da falha na implantação. Se um evento de erro 465 precedeu o evento 404, houve um problema ao abrir o pacote.

Se o erro 465 não ocorreu, consulte Geral Solução de problemas de empacotamento, implantação e consulta de Windows [aplicativos](troubleshooting.md). Caso contrário, consulte esta tabela para ver códigos de erro comuns que podem aparecer na cadeia de caracteres de erro para o evento de erro 465:

| Código do erro | Erro                                 | Descrição                                                                                                          | Sugestão                                                                                                                                                                                                 |
|------------|---------------------------------------|----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x80073CF0 | ERRO \_ AO INSTALAR O PACOTE ABERTO COM \_ \_ \_ FALHA | Não foi possível abrir o pacote do aplicativo.                                                                                 | Esse erro normalmente indica um problema com o pacote. Você precisa criar e assinar o pacote novamente. Para obter mais informações, consulte [Usando o Empacotador de Aplicativos](make-appx-package--makeappx-exe-.md). |
| 0x80080205 | APPX \_ E \_ \_ BLOCKMAP INVÁLIDO            | O pacote do aplicativo foi adulterado ou tem um mapa de bloco inválido.                                                  | O pacote está corrompido. Você precisa criar e assinar o pacote novamente. Para obter mais informações, consulte [Usando o Empacotador de Aplicativos](make-appx-package--makeappx-exe-.md).                                  |
| 0x800B0004 | TRUST \_ E \_ SUBJECT \_ NOT \_ TRUSTED       | O pacote do aplicativo foi adulterado.                                                                              | O conteúdo do pacote não corresponderá mais à sua assinatura digital. Você precisa assinar o pacote novamente. Para obter mais informações, [consulte Como assinar um pacote de aplicativos usando o SignTool.](how-to-sign-a-package-using-signtool.md)  |
| 0x800B0100 | TRUST \_ E \_ NAIGNATURE                 | O pacote do aplicativo não está assinado.                                                                                         | Somente pacotes Windows aplicativos assinados podem ser implantados. Para obter informações sobre como assinar um pacote de aplicativos, [consulte Como assinar um pacote de aplicativos usando o SignTool.](how-to-sign-a-package-using-signtool.md)                  |
| 0x800B0109 | CERT \_ E \_ UNTRUSTED \_ ROOT              | A cadeia de certificados usada para assinar o pacote de aplicativos termina em um certificado raiz que não é confiável.           | Continue para a Etapa 2 para solucionar problemas de confiança do certificado.                                                                                                                                                  |
| 0x800B010A | \_ENCADEAMENTO DE CERTIFICADO \_ E                     | Nenhuma cadeia de certificados pode ser criada para uma autoridade raiz confiável do certificado que foi usado para assinar o pacote do aplicativo. | Continue para a Etapa 2 para solucionar problemas de confiança do certificado.                                                                                                                                                  |



 

### <a name="step-2-determine-the-certificate-chain-used-to-sign-the-app-package"></a>Etapa 2: Determinar a cadeia de certificados usada para assinar o pacote do aplicativo

Para descobrir os certificados em que o computador local deve confiar, você pode examinar a cadeia de certificados para a assinatura digital no pacote do aplicativo.

**Para determinar a cadeia de certificados**

1.  No Explorador de Arquivos, clique com o botão direito do mouse no pacote do aplicativo e selecione **Propriedades**.
2.  Na caixa **de** diálogo Propriedades, selecione a **guia Assinaturas** Digitais, que também exibe se a assinatura pode ser validada.
3.  Na lista Assinatura, selecione a assinatura e clique no **botão** Detalhes.
4.  Na caixa **de diálogo Detalhes da Assinatura Digital,** clique no botão **Exibir** Certificado.
5.  Na caixa **de diálogo** Certificado, selecione a guia Caminho **de Certificação.**

O certificado superior na cadeia é o certificado raiz e o certificado inferior é o certificado de assinatura. Se apenas um único certificado estiver na cadeia, o certificado de assinatura também será seu próprio certificado raiz. Você pode determinar o número de série para cada certificado que você usa com [Certutil:](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc732443(v=ws.10))

**Para determinar o número de série para cada certificado**

1.  No painel Caminho de certificação, selecione o certificado e clique em **Exibir Certificado.**
2.  Na caixa de diálogo Certificado, selecione **a guia** Detalhes, que exibe o número de série e outras propriedades úteis do certificado.

### <a name="step-3-determine-the-certificates-trusted-by-the-local-machine"></a>Etapa 3: Determinar os certificados confiáveis pelo computador local

Para poder implantar um pacote de aplicativos, ele não só deve ser confiável no contexto do usuário, mas também no contexto do computador local. Como resultado, a assinatura digital pode aparecer válida quando exibida na guia Assinaturas Digitais da etapa anterior, mas ainda falhar na validação durante a implantação do pacote do aplicativo.

**Para determinar se a cadeia de certificados usada para assinar o pacote de aplicativos é especificamente confiável para o computador local**

1.  Execute este comando:

    ``` syntax
    CertUtil.exe -store Root rootCertSerialNumber
    ```

2.  Execute este comando:

    ``` syntax
    CertUtil.exe -store TrustedPeople signingCertSerialNumber
    ```

Se você não especificar o número de série do certificado, [o Certutil](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc732443(v=ws.10)) lista todos os certificados confiáveis pelo computador local para esse armazenamento.

O pacote pode não ser instalado devido a erros de encadeamento de certificados, mesmo se o certificado de assinatura não for auto-assinado e o certificado raiz estiver no armazenamento raiz do computador local. Nesse caso, pode haver um problema de confiança para as autoridades de certificação intermediárias. Para obter mais informações sobre esse problema, consulte [Trabalhando com certificados](/previous-versions/dotnet/netframework-3.0/ms731899(v=vs.85)).

## <a name="remarks"></a>Comentários

Se você determinou que o pacote não pôde ser implantado porque o certificado de assinatura não é confiável, não instale o pacote, a menos que você saiba de onde ele se originou e você confie nele.

Se você quiser confiar manualmente no aplicativo para instalação (por exemplo, para instalar seu próprio pacote de aplicativo assinado por teste), poderá adicionar manualmente o certificado à confiança do certificado do computador local do pacote do aplicativo.

**Para adicionar manualmente o certificado à confiança de certificado do computador local**

1.  No Explorador de Arquivos, clique com o botão direito do mouse no pacote do aplicativo e, no menu de contexto pop-up, selecione **Propriedades**.
2.  Na caixa **de** diálogo Propriedades, selecione a **guia Assinaturas** Digitais.
3.  Na lista Assinatura, selecione a assinatura e clique no **botão** Detalhes.
4.  Na caixa **de diálogo Detalhes da Assinatura Digital,** clique no botão **Exibir** Certificado.
5.  Na caixa **de diálogo** Certificado, clique em **Instalar Certificado...** .
6.  No Assistente de Importação de Certificados, selecione **Computador Local** e clique em **Próximo.** Você precisará conceder privilégios de administrador para continuar.
7.  Selecione **Colocar todos os certificados no armazenamento a seguir e** navegue até o armazenamento Pessoas **Confiáveis.**
8.  Clique **em Próximo** e em Concluir **para** concluir o assistente.

Após essa adição manual, você pode ver que o certificado agora é confiável na caixa **de diálogo** Certificado.

Você pode remover o certificado depois de não precisar mais dele.

**Para remover o certificado**

1.  Execute **Cmd.exe** como administrador.
2.  No prompt de comando do administrador, execute este comando:

    ``` syntax
    Certutil -store TrustedPeople
    ```

3.  Procure o número de série do certificado que você instalou. Esse número é *o certID.*
4.  Execute este comando:

    ``` syntax
    Certutil -delStore TrustedPeople certID
    ```

Recomendamos que você evite adicionar manualmente certificados raiz ao armazenamento de certificados de autoridades de certificação confiáveis do [computador](/windows-hardware/drivers/install/trusted-root-certification-authorities-certificate-store)local. Ter vários aplicativos assinados com certificados encadeados ao mesmo certificado raiz, como aplicativos de linha de negócios, pode ser mais eficiente do que instalar certificados individuais no armazenamento pessoas confiáveis. O armazenamento pessoas confiáveis contém certificados que são considerados confiáveis por padrão e, portanto, não são verificados por autoridades superiores, listas de confiança de certificado ou cadeias. Para considerações sobre como adicionar certificados ao armazenamento de certificados autoridades de certificação raiz confiáveis, consulte [Práticas recomendadas de assinatura de código.](/previous-versions/windows/hardware/design/dn653556(v=vs.85))

## <a name="security-considerations"></a>Considerações de segurança

Ao adicionar um certificado em [repositórios de certificados do computador local](/windows-hardware/drivers/install/local-machine-and-current-user-certificate-stores), você afetará a confiança do certificado de todos os usuários no computador. Recomendamos que você instale todos os certificados de assinatura de código que você deseja para testar pacotes de aplicativos no armazenamento de certificados pessoas confiáveis. Remova imediatamente esses certificados quando eles não são mais necessários, para impedir que eles sejam usados para comprometer a confiança do sistema. Se você criar seus próprios certificados de teste para assinar pacotes de aplicativos, também recomendamos restringir os privilégios associados ao certificado de teste. Para obter informações sobre como criar certificados de teste para assinar pacotes de aplicativos, consulte Como criar um certificado de assinatura [de pacote de aplicativo.](how-to-create-a-package-signing-certificate.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Amostras**
</dt> <dt>

[Criar exemplo de pacote de aplicativos](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/AppxPackingCreateAppx)
</dt> <dt>

**Conceitos**
</dt> <dt>

[Solucionar problemas de empacotamento, implantação e consulta de aplicativos Windows](troubleshooting.md)
</dt> <dt>

[Tarefas certutil para gerenciar certificados](/previous-versions/orphan-topics/ws.10/cc772898(v=ws.10))
</dt> </dl>

 

 
