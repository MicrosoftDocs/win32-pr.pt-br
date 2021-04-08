---
description: Lista os valores retornados por funções em APIs de autenticação.
ms.assetid: ea519e5c-98b0-4a01-b2cc-e5ff736a5396
title: Valores de retorno de autenticação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2831fbce55523b3d55a649ef18fb6a622f3ec0ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011250"
---
# <a name="authentication-return-values"></a>Valores de retorno de autenticação

## <a name="network-provider-values"></a>Valores do provedor de rede

A [API do provedor de rede](network-provider-api.md) usa os valores definidos a seguir.



| Valor                                                                           | Descrição                                               |
|---------------------------------------------------------------------------------|-----------------------------------------------------------|
| [Valores de retorno de segurança de rede](network-security-return-values.md)<br/> | Valores de retorno que um provedor de rede pode definir.<br/> |



 

## <a name="smart-card-return-values"></a>Valores de retorno do cartão inteligente

As [funções de cartão inteligente](authentication-functions.md) retornam os valores de retorno a seguir. Esses valores de retorno são definidos em Scarderr. h.

> [!Note]  
> Alguns valores de retorno podem ter o mesmo valor que os valores de retorno do Windows existentes que significam uma condição semelhante. Para obter informações sobre códigos de erro não listados aqui, consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).

 



| Valor                                                               | Descrição                                                                                                                                                                                                 |
|---------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ERRO \_ de \_ pipe interrompido<br/> 0x00000109<br/>                | O cliente tentou uma operação de cartão inteligente em uma sessão remota, como uma sessão de cliente em execução em um servidor de terminal, e o sistema operacional em uso não dá suporte ao redirecionamento de cartão inteligente.<br/> |
| SCARTAR \_ E \_ busca inadequada \_<br/> 0x80100029<br/>                | Ocorreu um erro ao definir o ponteiro do objeto de arquivo do cartão inteligente.<br/>                                                                                                                                 |
| SCARTAR \_ E \_ cancelado<br/> 0x80100002<br/>                | A ação foi cancelada por uma solicitação [**SCardCancel**](/windows/desktop/api/Winscard/nf-winscard-scardcancel) .<br/>                                                                                                                        |
| SCARTAR E não é possível \_ \_ \_ descartar<br/> 0x8010000E<br/>            | O sistema não pôde descartar a mídia da maneira solicitada.<br/>                                                                                                                               |
| \_cartão E \_ SCARTAR \_ sem suporte<br/> 0x8010001C<br/>        | O cartão inteligente não atende aos requisitos mínimos de suporte.<br/>                                                                                                                                   |
| SCARTAR \_ E \_ certificado \_ indisponível<br/> 0x8010002D<br/> | Não foi possível obter o certificado solicitado.<br/>                                                                                                                                                 |
| dados de SCARTAR \_ E de \_ comunicação \_ \_ perdidos<br/> 0x8010002F<br/>         | Foi detectado um erro de comunicação com o cartão inteligente. <br/>                                                                                                                                   |
| SCARTAR \_ E \_ dir \_ não \_ encontrados<br/> 0x80100023<br/>          | O diretório especificado não existe no cartão inteligente.<br/>                                                                                                                                        |
| SCARTAR \_ E \_ leitor duplicado \_<br/> 0x8010001B<br/>        | O driver do [*leitor*](/windows/desktop/SecGloss/r-gly) não produziu um nome de leitor exclusivo.<br/>                                                                            |
| \_arquivo scartar \_ E \_ não \_ encontrado<br/> 0x80100024<br/>         | O arquivo especificado não existe no cartão inteligente.<br/>                                                                                                                                             |
| CreateOrder do SCARTAR \_ E \_ ICC \_<br/> 0x80100021<br/>         | Não há suporte para a ordem solicitada de criação de objeto.<br/>                                                                                                                                         |
| instalação do SCARTAR \_ E \_ ICC \_<br/> 0x80100020<br/>        | Nenhum provedor primário pode ser encontrado para o cartão inteligente.<br/>                                                                                                                                             |
| SCARTAR \_ E \_ buffer insuficiente \_<br/> 0x80100008<br/>     | O buffer de dados para dados retornados é muito pequeno para os dados retornados.<br/>                                                                                                                            |
| \_ATR scartar E \_ inválido \_<br/> 0x80100015<br/>             | Uma [*cadeia de caracteres ATR*](/windows/desktop/SecGloss/a-gly) obtida do registro não é uma cadeia de caracteres ATR válida.<br/>                                                        |
| SCARTAR \_ E \_ \_ CHV inválido<br/> 0x8010002A<br/>             | O PIN fornecido está incorreto.<br/>                                                                                                                                                                   |
| SCARTAR \_ E \_ \_ identificador inválido<br/> 0x80100003<br/>          | O identificador fornecido não era válido.<br/>                                                                                                                                                               |
| SCARTAR \_ E \_ \_ parâmetro inválido<br/> 0x80100004<br/>       | Um ou mais dos parâmetros fornecidos não puderam ser adequadamente interpretados.<br/>                                                                                                                        |
| SCARTAR \_ E \_ \_ destino inválido<br/> 0x80100005<br/>          | As informações de inicialização do registro estão ausentes ou não são válidas.<br/>                                                                                                                                            |
| SCARTAR \_ E \_ \_ valor inválido<br/> 0x80100011<br/>           | Um ou mais dos valores de parâmetro fornecidos não puderam ser adequadamente interpretados.<br/>                                                                                                                  |
| SCARTAR \_ E \_ sem \_ acesso<br/> 0x80100027<br/>               | Acesso negado ao arquivo.<br/>                                                                                                                                                                    |
| SCARTAR \_ E \_ no \_ dir<br/> 0x80100025<br/>                  | O caminho fornecido não representa um diretório de cartão inteligente.<br/>                                                                                                                                     |
| SCARTAR \_ E \_ nenhum \_ arquivo<br/> 0x80100026<br/>                 | O caminho fornecido não representa um arquivo de cartão inteligente.<br/>                                                                                                                                          |
| SCARTAR \_ E \_ nenhum \_ contêiner de chave \_<br/> 0x80100030<br/>       | O contêiner de chave solicitado não existe no cartão inteligente.<br/>                                                                                                                                    |
| SCARTAR \_ E \_ sem \_ memória<br/> 0x80100006<br/>               | Não há memória suficiente disponível para concluir este comando.<br/>                                                                                                                                            |
| SCARTAR \_ E \_ nenhum \_ cache de PIN \_<br/> 0x80100033<br/>           | O PIN do cartão inteligente não pode ser armazenado em cache.<br/> **Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Este código de erro não está disponível.<br/> <br/>                        |
| SCARTAR \_ E \_ nenhum \_ leitor \_ disponível<br/> 0x8010002E<br/>   | Nenhum leitor de cartão inteligente está disponível.<br/>                                                                                                                                                               |
| SCARTAR \_ E \_ nenhum \_ serviço<br/> 0x8010001D<br/>              | O Gerenciador de [*recursos*](/windows/desktop/SecGloss/r-gly) de cartão inteligente não está em execução.<br/>                                                                |
| SCARTAR \_ E \_ sem \_ cartão inteligente<br/> 0x8010000C<br/>            | A operação requer um cartão inteligente, mas nenhum cartão inteligente está atualmente no dispositivo.<br/>                                                                                                               |
| SCARTAR \_ E \_ não há \_ tal \_ certificado<br/> 0x8010002C<br/>    | O certificado solicitado não existe.<br/>                                                                                                                                                        |
| SCARTAR \_ E \_ não \_ está pronto<br/> 0x80100010<br/>               | O leitor ou o cartão não está pronto para aceitar comandos.<br/>                                                                                                                                              |
| SCARTAR \_ E \_ não \_ transacionado<br/> 0x80100016<br/>          | Foi feita uma tentativa de encerrar uma transação inexistente.<br/>                                                                                                                                            |
| SCARTAR \_ E \_ PCI \_ muito \_ pequeno<br/> 0x80100019<br/>          | O buffer de recebimento de PCI era muito pequeno.<br/>                                                                                                                                                            |
| \_cache de PIN scartar E \_ \_ \_ expirado<br/> 0x80100032<br/>      | O cache de PIN do cartão inteligente expirou.<br/> **Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Este código de erro não está disponível.<br/> <br/>                       |
| incompatibilidade de SCARTAR \_ E \_ proto \_<br/> 0x8010000F<br/>          | Os protocolos solicitados são incompatíveis com o protocolo atualmente em uso com o cartão.<br/>                                                                                                       |
| SCARTAR \_ E \_ \_ cartão somente \_ leitura<br/> 0x80100034<br/>         | O cartão inteligente é somente leitura e não pode ser gravado.<br/> **Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Este código de erro não está disponível.<br/> <br/>       |
| SCARTAR \_ E \_ leitor \_ não disponíveis<br/> 0x80100017<br/>      | O leitor especificado não está disponível para uso no momento.<br/>                                                                                                                                         |
| leitor de SCARTAR \_ E \_ \_ sem suporte<br/> 0x8010001A<br/>      | O driver do leitor não atende aos requisitos mínimos de suporte.<br/>                                                                                                                                |
| SCARTAR \_ E \_ servidor \_ muito \_ ocupado<br/> 0x80100031<br/>        | O Gerenciador de recursos de cartão inteligente está muito ocupado para concluir esta operação.<br/>                                                                                                                          |
| SCARTAR \_ E \_ serviço \_ parado<br/> 0x8010001E<br/>         | O Gerenciador de recursos de cartão inteligente foi desligado.<br/>                                                                                                                                                   |
| SCARTAR \_ E \_ violação de compartilhamento \_<br/> 0x8010000B<br/>       | O cartão inteligente não pode ser acessado devido a outras conexões pendentes.<br/>                                                                                                                      |
| SCARTAR \_ E \_ sistema \_ cancelado<br/> 0x80100012<br/>        | A ação foi cancelada pelo sistema, supostamente para fazer logoff ou desligar.<br/>                                                                                                                       |
| \_ \_ tempo limite de scartar E<br/> 0x8010000A<br/>                  | O valor de tempo limite especificado pelo usuário expirou.<br/>                                                                                                                                                   |
| SCARTAR \_ E \_ inesperado<br/> 0x8010001F<br/>               | Ocorreu um erro inesperado de cartão.<br/>                                                                                                                                                           |
| \_cartão scartar E \_ desconhecido \_<br/> 0x8010000D<br/>            | O nome do cartão inteligente especificado não é reconhecido.<br/>                                                                                                                                                 |
| \_leitor scartar E \_ desconhecido \_<br/> 0x80100009<br/>          | O nome do leitor especificado não é reconhecido.<br/>                                                                                                                                                     |
| SCARTAR \_ E \_ \_ res MNG de resolução desconhecida \_<br/> 0x8010002B<br/>        | Um código de erro não reconhecido foi retornado.<br/>                                                                                                                                                         |
| \_recurso scartar E \_ sem suporte \_<br/> 0x80100022<br/>     | Este cartão inteligente não oferece suporte ao recurso solicitado.<br/>                                                                                                                                          |
| SCARTAR \_ E \_ gravar \_ \_ muitos<br/> 0x80100028<br/>         | Foi feita uma tentativa de gravar mais dados do que se ajustaria no objeto de destino.<br/>                                                                                                                      |
| \_erro scartar F \_ comm \_<br/> 0x80100013<br/>              | Foi detectado um erro de comunicação interno.<br/>                                                                                                                                              |
| \_ \_ erro interno de scartar F \_<br/> 0x80100001<br/>          | Falha na verificação de consistência interna.<br/>                                                                                                                                                            |
| SCARTAR \_ F \_ \_ erro desconhecido<br/> 0x80100014<br/>           | Um erro interno foi detectado, mas a origem é desconhecida.<br/>                                                                                                                                  |
| SCARTAR \_ F \_ aguardou \_ muito \_ tempo<br/> 0x80100007<br/>        | Um temporizador de consistência interno expirou.<br/>                                                                                                                                                       |
| desligamento do SCARTAR \_ P \_<br/> 0x80100018<br/>                 | A operação foi anulada para permitir que o aplicativo de servidor seja encerrado.<br/>                                                                                                                          |
| SCARTAR \_ S com \_ êxito<br/>                                        | Nenhum erro foi encontrado.<br/>                                                                                                                                                                        |
| SCARTAR \_ W \_ cancelado \_ pelo \_ usuário<br/> 0x8010006E<br/>      | A ação foi cancelada pelo usuário.<br/>                                                                                                                                                             |
| \_item de cache scartar W \_ \_ \_ não \_ encontrado<br/> 0x80100070<br/>  | O item solicitado não foi encontrado no cache.<br/>                                                                                                                                              |
| \_item de \_ cache scartar W \_ \_ obsoleto<br/> 0x80100071<br/>       | O item de cache solicitado é muito antigo e foi excluído do cache.<br/>                                                                                                                              |
| \_item de cache scartar W \_ \_ \_ muito \_ grande<br/> 0x80100072<br/>    | O novo item de cache excede o tamanho máximo por item definido para o cache.<br/>                                                                                                                      |
| \_cartão scartar \_ W \_ não \_ autenticado<br/> 0x8010006F<br/> | Nenhum PIN foi apresentado ao cartão inteligente.<br/>                                                                                                                                                          |
| SCARTAR \_ W \_ CHV \_ bloqueado<br/> 0x8010006C<br/>             | O cartão não pode ser acessado porque o número máximo de tentativas de entrada de PIN foi atingido.<br/>                                                                                                   |
| \_EOF scartar W \_<br/> 0x8010006D<br/>                      | O fim do arquivo de cartão inteligente foi atingido.<br/>                                                                                                                                                 |
| \_ \_ cartão removido do scartar W \_<br/> 0x80100069<br/>            | O cartão inteligente foi removido, portanto a comunicação adicional não é possível.<br/>                                                                                                                       |
| \_cartão de \_ redefinição de scartar W \_<br/> 0x80100068<br/>              | O cartão inteligente foi redefinido.<br/>                                                                                                                                                                        |
| \_violação de \_ segurança scartar W \_<br/> 0x8010006A<br/>      | O acesso foi negado devido a uma violação de segurança.<br/>                                                                                                                                               |
| cartão de SCARTAR \_ W sem \_ energia \_<br/> 0x80100067<br/>          | A energia foi removida do cartão inteligente, para que a comunicação adicional não seja possível.<br/>                                                                                                       |
| cartão sem resposta do SCARTAR \_ W \_ \_<br/> 0x80100066<br/>       | O cartão inteligente não está respondendo a uma redefinição.<br/>                                                                                                                                                     |
| \_ \_ cartão sem suporte do scartar \_ W<br/> 0x80100065<br/>        | O leitor não pode se comunicar com o cartão devido a conflitos de configuração de cadeia de caracteres ATR.<br/>                                                                                                          |
| SCARTAR \_ W \_ CHV incorreto \_<br/> 0x8010006B<br/>               | O cartão não pode ser acessado porque foi apresentado um PIN incorreto.<br/>                                                                                                                                 |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Códigos de erro do sistema](/windows/desktop/Debug/system-error-codes)
</dt> </dl>

 

